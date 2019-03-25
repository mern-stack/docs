---
id: email
title: Email
sidebar_label: Email
---

Sending Email is a very easy in this project, you dont have to worry about much configuration -

## Configuration
    Email configuration is in .env file

*By Default .pug files are used as email template.*

## Sending Email
```js
const mail = require("../email");

let user = {};
  user.email = "hello@gma.com";
  mail.send({
    user,
    subject: "your subject",
    filename: "my-email-view"
  });
```
 
### Subject Of Email
For subject of email  add `subject` in `mail.send()`
 for example

```js
const mail = require("../email");

let user = {};
  user.email = "hello@gma.com";
  mail.send({
    ...
    subject: "My New Subject",
    ...
  });
```

### View of Email
For Vies of email  add `filename` in `mail.send()`
 for example

```js
const mail = require("../email");

let user = {};
  user.email = "hello@gma.com";
  mail.send({
    ...
    filename: "welcome",
    ...
  });
  // here welcome should be inside `app/views/email/welcome.pug`
```

### Sendind data in email
For sending data to email  add `variable` in `mail.send()`
 for example

```js
const mail = require("../email");

let user = {};
  user.email = "hello@gma.com";
  mail.send({
    ...
    ceo: "Kumar Ravi",
    manager: "Ankit Singh",
    Lead : "Ankit Chauhan"
    ...
  });
  // and in your view render as
  #{ceo} #{manager} #{lead}
```
