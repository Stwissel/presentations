##  The pipe

- bitbucket-pipelines.yml
- environment variables (eventually)

```
# Build the blog and push it back
clone:
  depth: 1
pipelines:
  branches:
    master:
      - step:
          script:
            - echo "Executing build"
            - chmod +x ./bbbuild.sh
            - ./bbbuild.sh
```

