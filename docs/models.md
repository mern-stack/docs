---
id: models
title: Models
sidebar_label: Models
---

Models Provide Clean Interface to interact with your MongoDB database through moongoose library.

## Creating Models 
Models Can be created in two ways :

### Through Command Line
Models Can Be Created From Command Line :
First Run - 
```bash
node artisan
```
then 
```bash
make:model <Name-of-your-model>
```

We don't have any restrictions on naming your Models, But the preferred way of creating Models is -
`NameOfYourModel` for example:-
```bash
make:model Users
```
This will automatically create your model in `app\models` Directory and migration in 
`app\database\migrations` directory


### Manually

Models can be created manually also-

1. Create a file name of your choice in `app\models`
2. Create Migration in `app\database\migrations` 
    example: - You have created a model - User.js
    ```js
        const mongoose = require("mongoose");

    ```
3. Now Create a schema in `app\database\migrations` directory
    example:- You have created  `create_Users_model.js` in `app\database\migrations`
4. Now in your `app\models\User.js`
    ```js
        const mongoose = require("mongoose");
        const UsersObject = require("../../database/migrations/create_Users_model");

        const Users = mongoose.model("Users", new mongoose.Schema(UsersObject));

        module.exports = Users;
    ```
 5. Done !!! Enjoy !   

of course if you create a model from CLI, we will take care of everything.