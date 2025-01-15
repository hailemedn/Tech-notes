24.10.29  05.41  
tags:[[web]] [[backend]] [[security]] 


# Using passport.js to add cookies and sessions
## install
```sh
$ npm i passport express-session passport-local-mongoose
```
## require
```js
const session = require("express-session");
const passport = require("passport");
const passportLocalMongoose = require("passport-local-mongoose");
```


```js
app.use(session({
  secret: "our little secret.",
  resave: false,
  saveUninitialized: false,
}));

app.use(passport.initialize());
app.use(passport.session());
```


```js
const userSchema = new mongoose.Schema({
    email: String,
    password: String,
  });

  userSchema.plugin(passportLocalMongoose);
```


```js
const User = mongoose.model("User", userSchema);

  // CHANGE: USE "createStrategy" INSTEAD OF "authenticate"
  passport.use(User.createStrategy());

  passport.serializeUser(User.serializeUser());
  passport.deserializeUser(User.deserializeUser());
```



## register
```js
app.post("/register", async (req, res) => {
    User.register({username: req.body.username}, req.body.password, function(err, user) {
      if(err) {
        console.log(err);
        res.redirect('/register');
      } else {
        passport.authenticate("local")(req, res, function() {
          res.redirect("/secrets");
        });
      }
    });
  });
```


## login
```js
  app.post("/login", async (req, res) => {
    const user = new User({
      username: req.body.username,
      password: req.body.password,
    });

    req.login(user, function(err) {
      if(err) {
        console.log(err);
      } else {
        res.redirect("/secrets");
      }
    });
  });
```


## logout 

we use get for this bc, the html is an anchor tag, the others use post because they are inside a form and we use the inputs values.

```html
<a class="btn btn-light btn-lg" href="/logout" role="button">Log Out</a>
```

```js
app.get("/logout", (req, res) => {
    req.logout(function (err) {
      if(err) {
        console.log(err);
      } else {
        res.redirect("/login");
      }
    });
  });
```



# Reference
[[The Complete 2023 Web Development Bootcamp]]
[[Level 5 - Cookies and Sessions]]
[[Authentication & Security]]
