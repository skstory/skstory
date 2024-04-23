---
layout: post
title: "install node.js accoding to version & Express.js"
---

1. Enter the site <a> https://github.com/coreybutler/nvm-windows/releases - click 'nvm-setup.exe' - install

   ![alt text](image.png)

1. Enter 'nvm install ‘desired version’' in the cmd command prompt

   ![alt text](image-2.png)

1. Enter 'nvm use 20.10.0'

1. Install node js

   > npx create-next-app@latest
   > ![alt text](image-3.png)

1. Enter 'npm run dev' in VS code terminal
   ![alt text](image-4.png)

> click 'http://localhost:3000' + ctrl

![alt text](image-5.png)

5-1. Enter 'npm install' before entering 'npm run dev' when starting from a new folder

## When Node.js is already installed

1. in termial

   > mkdir "folder name"
   > cd "folder name"
   > npm init

   ![alt text](image-7.png)

   => created 'package.json'

2. create 'index.js'

## Install Express.js

3. install express.js

   > npm install express --save
   > ![alt text](image-8.png)

4. create'app.js' and copy this

   ```js
   const express = require("express");

   const app = express();

   app.use((req, res) => {
     res.json({ message: "votre requete a bien ete recue" });
   });

   module.exports = app;
   ```

5. copy in 'server.js'

   ```js
   const http = require("http");
   const app = require("./app");

   app.set("port", process.env.PORT || 3000);
   const server = http.createServer(app);

   server.listen(process.env.PORT || 3000);
   ```

6. add 'start: node index.js' in package.json

![alt text](image-9.png)

6. in terminal
   > npm run start
