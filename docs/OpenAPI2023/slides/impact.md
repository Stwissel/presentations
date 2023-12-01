## Classic

```java
@Route(path = "/some/:category/:name",
        methods = HttpMethod.POST)
public void createCategoryMember(@Param String category,
                                 @Param String name,
                                RoutingExchange ctx) {
    if (isValid(category)) {
      // your code goes here
    }
 }
```

---

## OpenAPI

```java
routerBuilder.getRoute("makeCatMember")
     .addRoute(Utils::logger)
     .addRoute(Categories::addMember)
     .addFailureHandler(Screwups::route);
```

---

## Eventbus dynamic example

```java
void init() {
   JsonObject spec = Utils.jsonFromResource(OPENAPI);
   OpenAPIContract contract = OpenAPIContract
            .from(this.getVertx(), spec).await();
   RouterBuilder builder =RouterBuilder
            .create(this.getVertx(), contract);
   builder.getRoutes().forEach(this::setupRoute);
}
```

---

```java
void setupRoute(OpenAPIRoute route) {
    Operation operation = route.getOperation();
    Eventbus eb = this.vertx.eventBus();
    route.addHandler(ctx -> {
       ValidatedRequest request = ctx
        .get(RouterBuilder.KEY_META_DATA_VALIDATED_REQUEST);
       eb.request(operation.getOperationId, request)
          .onSuccess(msg -> ctx.end(msg.body()))
          .onFailure(err -> bringSadNews(ctx, err));
    })
}
```
