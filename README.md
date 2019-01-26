# A ROOM WITH A VIEW

## Project setup - Development
+ Fork & Clone Directory
+ Install yarn on your computer: ```brew install yarn```
If you do not use homebrew [follow these alternative instructions](https://yarnpkg.com/lang/en/docs/install/#mac-stable)
+ Make sure you have the most up to date version of node ( > 8 to use vue ```node -v```) ```brew install nvm && nvm install node ```
      check which node versions are installed ```nvm ls```
      switch to the one you would like to use ```nvm use <version-num> ```
+ Install yarn in project directory ```yarn install```
+ Start a server so that you can view your work ```yarn run serve```
+ When your server is running it will tell you where to view your work. For me it is: (http://localhost:8080/)

<!-- ### Compiles and minifies for production ```yarn run build``` -->

## Vue.js NOTES

<!-- What does main.js do?  -->
#### App.vue
+ <template> Holds all the main components of the app - the window and the pool <!-- should the pool actually be inside the window?  -->
+ <script> Imports the components from the file tree then then exports components to the <template>.
+ <style> connects the scss files
