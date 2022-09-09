# ninja-food

Setup

Step 1: 
npm init -y 
get: package .json file

Step 2:
npm install -D tailwindcss
get: node_modules for tailwind

Step 3:
npx tailwind init
get: tailwind.config.js

Step 4: Add location of source html file in content of tailwind.config.js
example:
module.exports = {
  content: ["./src/**/*.{html,js}"],
 or 
module.exports = {
 content: ['./*.html'],
 
 Step 5: Make a input.css file and paste

@tailwind base;
@tailwind components;
@tailwind utilities;

Can add custom css to this file

Step 6: Open Package .json file and add the following script for build and watch

  "scripts": {
    "build": "tailwindcss -i ./src/input.css -o ./css/main.css",
    "watch": "tailwindcss -i ./src/input.css -o ./css/main.css --watch"
  },
  
input is the file we just made in step 5 and output is main file

Step 7: Test by running, it will make optput css file;
npm run build

Step 8: Add link in the html to the main.css file
<link rel="stylesheet" href="main.css">

Step 9: Constantly watch:
npm run watch

Step 10: Open with live server


  
