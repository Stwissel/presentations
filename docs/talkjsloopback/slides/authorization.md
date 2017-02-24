##  Authorization

- named roles
- $everyone, $authenticated, $unauthenticated
- READ, WRITE, EXECUTE

      {
      "accessType": "EXECUTE",
      "principalType": "ROLE",
      "principalId": "$everyone",
      "permission": "ALLOW",
      "property": "provideSMSToken"
      }

source: https://docs.strongloop.com/display/public/LB/Controlling+data+access