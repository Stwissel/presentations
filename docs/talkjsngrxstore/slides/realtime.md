## Realtime enablement

### App Component
```
  ngOnInit() {
    this.memberService.listenToTheSocket().subscribe((result: any) => {
        const member: Member = JSON.parse(result);
        this.store.dispatch(new MemberActions.AddMember(member));
    })
  }
```

### Service
```
  listenToTheSocket(): Observable<any> {
    this.websocket = new WebSocket("wss://someurl");
    return Observable.create(observer => {
      this.websocket.onmessage = (evt) => {
        observer.next(evt);
      };
    }).map(res => res.data).share();
  }
```