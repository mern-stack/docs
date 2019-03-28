---
id: installation
title: Installation
sidebar_label: Installation
---

1. Open terminal of your choice and type

```bash
git clone https://github.com/mern-stack/mern.git <Your-Project-Name>
```

2. CD into the `<Your-Project-Name>/backend` directory and rename `.env.example to .env`

3. Enter `PORT` number to port of your choice, for example `PORT=5000`.

        This will be used for running server on the specified port

4. Enter a secure random string to `KEY=` in `.env`
        
    You can get a secure key from [Generate Random Key](http://www.allkeysgenerator.com/Random/Security-Encryption-Key-Generator.aspx)

    *It Is recommended to generate 256 bit Key*

5. Now go to root of your project and run `npm run setup` in your terminal and we will set everything for you.
