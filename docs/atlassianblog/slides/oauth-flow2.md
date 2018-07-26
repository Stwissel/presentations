##  OAuth result

- Receive `access_token` to use as Bearer
```
{
	"access_token": "some long string",
	"scopes": "pullrequest:write repository:admin",
	"expires_in": 7200,
	"refresh_token": "not so long string",
	"token_type": "bearer"
}
```
- POST comment payload
 https://api.bitbucket.org/2.0/repositories/org/repo/src