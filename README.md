# Creating a Micro Frontend - Guide

Follow the next steps:

### Create an isolated component

1. Create a new folder, inside that folder run the command:
   ```bash
   npm init -y
   ```
2. Then install the following packages by running the next command:
   ```bash
   npm install webpack@5.4.0 webpack-cli@4.3.0 webpack-dev-server@3.11.0 html-webpack-plugin@4.5.0
   ```
3. Inside the `package.json`, modify the scripts section:
   ```json
   {
   ...
   "scripts": {
       "start": "webpack"
     },
   }
   ```
4. Create a file for webpack configuration: `webpack.config.js` and set the main configuration for the project.
   ```js
   const HtmlWebpackPlugin = require("html-webpack-plugin");

   module.exports = {
     mode: "development",
     devServer: {
       port: 8080,
     },
     plugins: [
       new HtmlWebpackPlugin({
         template: "./public/index.html",
       }),
     ],
   };
   ```
5. Create the main javascript, first you have to create a new folder called `src` and then create the file `index.js`
6. Run the command `npm run start`. Webpack will create a new `dist` directory, here you'll find the files `main.js` and `index.html`, those file represent your bundled project.
7. Next change the `package.json` to run a development server on the port that you defined  inside the `webpack.config.js` file.
   ```js
   {
   ...
   "scripts": {
       "start": "webpack serve"
     },
   }
   ```
8.

### Create the container main project

1. Repeat the previous steps.  You need to have
