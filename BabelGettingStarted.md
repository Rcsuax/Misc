##GettingStarted With Babel

http://www.programwitherik.com/understanding-the-babel-compiler-2016/

###package.json
```javascript
{
  "name": "es",
  "version": "1.0.0",
  "description": "",
  "main": "app.js",
  "scripts": {
    "build": "babel src -d build",
    "clean": "rm build/* -r",
    "deep-clean": "rm node_modules -r && npm install",
    "dev": "nodemon ./build/app.js",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "babel-cli": "^6.18.0",
    "babel-preset-es2015": "^6.18.0",
    "nodemon": "^1.11.0"
  }
}
```


###.babelrc
```javascript
{
  "presets": ["es2015"]
}
```
