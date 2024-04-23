---
layout: post
title: "MongoDB & mongoose"
---

MongoDB : database NoSQL
Mongoose : a package that facilitates interactions with our MongoDB database

1.  > npm install mongoose --save

![alt text](image-10.png)

2. in index.js

![alt text](image-11.png)

3.  > npm run start

![alt text](image-12.png)

4. in 'app.js'

```js
const mongoose = require("mongoose");

mongoose
  .connect("mongodb+srv://skstory:hello1234@skstory.pnjwiaw.mongodb.net/")
  .then(() => console.log("connexion a mongoDB reussie!"))
  .catch(() => console.log("connexion a mongoDB echouee"));
```
