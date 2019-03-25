---
id: authentication
title: Authentication
sidebar_label: Authentication
---

Authentication is based on `passport` and built on top of `Json Web Token (JWT)`.

If you dont know about Json Web Token, you can read it from [Here](https://jwt.io)

## Passport Strategy

Strategy of passport is located in `config\passport.js` file.

This uses `jwt-strategy` of passport, you can use more strategies from [Passport Strategies](http://www.passportjs.org/packages/)

## Database Consideration
We are using Users Model for authentication,user can login via email and password.

## Change Default Login 
You can change default login style from `app/http/controllers/auth/loginController.js`
