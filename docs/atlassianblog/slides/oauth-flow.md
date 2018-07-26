##  OAuth Flow

- Post to `bitbucket.org` (Powered by nginx)

```
POST /site/oauth2/access_token
content-type: application/x-www-form-urlencoded
authorization: Basic Base64(client_id:client_secret)
accept: */*
host: bitbucket.org
accept-encoding: gzip, deflate
content-length: 65
```

### Body:

```
grant_type=client_credentials
scope=
client_id=clientidstring
```
