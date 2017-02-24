##  Think MODELS!

A model consists of a JSON and a JS file
- relations & access control
- structure & behavior

      Member.remoteMethod(
        'requestSMSLogin', {
          accepts: { arg: 'mobilenumber', type: 'string',
            description: 'Phone number including +65 and no spaces' },
          returns: { arg: 'Status', type: 'string' },
          description: 'request for an SMS token to login',
          http: { path: '/requestsmstoken', verb: 'post' },
          isStatic: true }
      );

Automatic REST