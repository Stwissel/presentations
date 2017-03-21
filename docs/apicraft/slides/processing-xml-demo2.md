##  XML @Annotations

```
@XmlRootElement(name = "SomeName")
@XmlElement(name = "SomeName")
```

```
JAXBContext context = JAXBContext.newInstance(BookingList.class);
Marshaller m = context.createMarshaller();
m.setProperty(Marshaller.JAXB_FORMATTED_OUTPUT, Boolean.TRUE);
m.marshal(this, out);
```
