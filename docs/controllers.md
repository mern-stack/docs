---
id: controllers
title: Controllers
sidebar_label: Controllers
---

Instead of defining all of your request handling logic as Closures in route files, you may wish to organize this behavior using Controller classes. Controllers can group related request handling logic into a single class. Controllers are stored in the app/Http/Controllers directory.

## Creating Controllers 
Controllers Can be created in two ways :

### Through Command Line
Controllers Can Be Created From Command Line :
First Run - 
```bash
node artisan
```
then 
```bash
make:controller <Name-of-your-Controller>
```

We don't have any restrictions on naming your controllers, But the preferred way of creating controllers is -
`nameOfYourWishController` for example:-
```bash
make:controller UsersController
```
This will automatically create your controller in `app\Http\Controllers` Directory and register your controller in 
`app\providers\controllerProvider.js`


### Manually

Controllers can be created manually also-

1. Create a file name of your choice in `app\Http\Controllers`
2. Register your controller in `app\providers\controllerProvider.js` 
    example: - You have created a controller - userController.js
    ```js
    const main = {};

    main.userController = require("../http/controllers/userController");

    module.exports = main;

    ```
3. Thats it !!

of course if you create a controller from CLI, we will take care of everything.