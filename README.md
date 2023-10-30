﻿# calculator-server

- In project folder create **calculator.js** 
- Set up a new NPM package

```
$ npm init
```

- Using NPM install the express module
```
$ npm install express
```

- Install npm body-parser package
```
$ npm install body-parser
```

- Require express and body-parser in your calculator.js
```
  const express = require('express');
  const app = express();
  const bodyParser = require("body-parser");
  
  app.use(bodyParser.urlencoded({extended: true}));

```

- Use app.get to set-up file to localhost
```
app.get("/", function(req, res) {
  res.sendFile(__dirname + "/index.html");
});
```

- use app.post() to add functionality to user interaction
````
  
  app.post("/", function(req, res) {
  
    var num1 = Number(req.body.num1);    // body-parser parsing
    var num2 = Number(req.body.num2);
    var result = num1 + num2;
  
    res.send("The result of calculation: " + result);
  });

````

- Install **nodemon**
```
npm install -g nodemon
```
