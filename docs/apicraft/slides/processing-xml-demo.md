##  Parse XML in Java

```
DocumentBuilderFactory factory = DocumentBuilderFactory.newInstance(); factory.setValidating(false);
factory.setNamespaceAware(true);
InputSource source = new InputSource(new StringReader(sourceString));
DocumentBuilder docb = factory.newDocumentBuilder();
Document d = docb.parse(source);
```
