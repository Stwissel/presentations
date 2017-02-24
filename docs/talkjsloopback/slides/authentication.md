##  Authentication

- based on JSON Web Token
- compatible to Passport
- Extensible

       Member.createAccessToken(timetolive, function(err, accesstoken) {
          cb(err, accesstoken);
       })