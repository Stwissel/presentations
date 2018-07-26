##  Pull request

- /2.0/repositories/org/repo/pullrequests/
- Host: api.bitbucket.org
- Content-Type: **application/json**
- Authorization: Bearer access_token

### Body

```
{
	"title" : "Name of pull request",
	"source" : {
		"branch": {
			"name" : "comments"
		},
		"repository" : {
			"full_name" : "org/repo"
		}
	},
	"destination" : {
		"branch" : {
			"name" : "master"
		}
	}
	"close_source_branch" : true	
}
```
