##GettingStarted With Babel

http://www.programwitherik.com/understanding-the-babel-compiler-2016/

###package.json
{
  "name": "es",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "build": "babel src -d lib",
    "repl": "./node_modules/.bin/babel-node",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "rcsuax",
  "license": "ISC",
  "devDependencies": {
    "babel-cli": "^6.18.0",
    "babel-preset-es2015": "^6.18.0"
  }
}

###.babelrc
{
  "presets": ["es2015"]
}
