##  Getting started
### Machine translation

https://www.ng.bluemix.net/docs/#services/MachineTranslation/index.html

```
String post = "rt=text&sid=" + URLEncoder.encode(sid, "UTF-8") +
    "&txt=" + URLEncoder.encode(text, "UTF-8");
  HttpURLConnection conn = (HttpURLConnection)new URL(endpoint).openConnection();
  conn.connect();
```
