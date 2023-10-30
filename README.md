# calculator-server

1. In project folder create **calculator.js** 
2. Set up a new NPM package

```
$ npm init
```

3. Using NPM install the express module
```
$ npm install express
```

4. Install npm body-parser package
```
$ npm install body-parser
```

5. Require express and body-parser in your calculator.js
```
  const express = require('express');
  const app = express();
  const bodyParser = require("body-parser");
  
  app.use(bodyParser.urlencoded({extended: true}));

```

6. Use app.get to set-up file to localhost
```
app.get("/", function(req, res) {
  res.sendFile(__dirname + "/index.html");
});
```

7. use app.post() to add functionality to user interaction
````
  
  app.post("/", function(req, res) {
  
    var num1 = Number(req.body.num1);    // body-parser parsing
    var num2 = Number(req.body.num2);
    var result = num1 + num2;
  
    res.send("The result of calculation: " + result);
  });

````

8. Start server to port 3000
````
    app.listen(3000, function() {
      console.log("App running at port 3000");
    });

````

9. Install **nodemon**
```
npm install -g nodemon
```

10. run server through terninal
````
nodemon calculator.js
````


__ Developed by: Abdul Mukit __
