# NativeScript Email

An Email module for use in NativeScript apps.
You can use it to compose emails, edit the draft manually, and send it.

## Installation
From the command prompt go to your app's `app` folder and execute:

```
npm install nativescript-email
```

## Usage

### available

```js
  var email = require( "./node_modules/nativescript-email/email" );

  email.available().then(function(avail) {
      alert("Avail? " + avail);
  })
```

### compose
```js
  var email = require( "./node_modules/nativescript-email/email" );

  email.compose({
      subject: "Yo",
      body: "Hello <strong>dude</strong> :)",
      to: ['eddyverbruggen@gmail.com', 'to@person2.com'],
      cc: ['eddyverbruggen@triodos.nl'],
      bcc: ['eddy@combidesk.com', 'eddy@x-services.nl']
  }).then(function(r) {
      console.log("email closed");
  });
```

## Known issues
On Android, you can pass an array of to/cc/bcc, but only the first one is added.

## Future work
Add attachment support

Fix the known issues :)