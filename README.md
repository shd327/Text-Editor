# Text Editor

## Siddharth Desai

This project covers J.A.T.E (ust another text editor). JATE is a text editor that runs in the browser. This is a single-page application that meets the PWA criteria. One important concept from this project I learned was leveraging service workers. I was able to leverage to cache static CSS, JavaScript, HTML files, images, and even API requests. This allows developers to reduce network bandwidth and improve overall load times.

[![License](https://img.shields.io/badge/License-BSD_2--Clause-orange.svg)](https://opensource.org/licenses/BSD-2-Clause)
## Table of Contents
1. [ User Story. ](#user_Story)
2. [ Acceptance Citeria. ](#acceptance_criteria)
3. [ Description. ](#description)
4. [ Installation. ](#installation)
5. [ Usage. ](#usage)
6. [ License. ](#license)
7. [ Screenshots. ](#screenshots)
8. [ Questions. ](#questions)
9. [ Links. ](#links)
10. [ Resources. ](#resources)

## User Story

```md
AS A developer
I WANT to create notes or code snippets with or without an internet connection
SO THAT I can reliably retrieve them for later use
```

## Acceptance Criteria

```md
GIVEN a text editor web application
WHEN I open my application in my editor
THEN I should see a client server folder structure
WHEN I run `npm run start` from the root directory
THEN I find that my application should start up the backend and serve the client
WHEN I run the text editor application from my terminal
THEN I find that my JavaScript files have been bundled using webpack
WHEN I run my webpack plugins
THEN I find that I have a generated HTML file, service worker, and a manifest file
WHEN I use next-gen JavaScript in my application
THEN I find that the text editor still functions in the browser without errors
WHEN I open the text editor
THEN I find that IndexedDB has immediately created a database storage
WHEN I enter content and subsequently click off of the DOM window
THEN I find that the content in the text editor has been saved with IndexedDB
WHEN I reopen the text editor after closing it
THEN I find that the content in the text editor has been retrieved from our IndexedDB
WHEN I click on the Install button
THEN I download my web application as an icon on my desktop
WHEN I load my web application
THEN I should have a registered service worker using workbox
WHEN I register a service worker
THEN I should have my static assets pre cached upon loading along with subsequent pages and static assets
WHEN I deploy to Heroku
THEN I should have proper build scripts for a webpack application
```

## Installation

* Clone the repository using:
```
git@github.com:shd327/Text-Editor.git
```
* Ensure you are in the current working directory
* Ensure all dependencies are installed as shown below installation instructions are below:
```
{
    "devDependencies": {
    "@babel/core": "^7.15.0",
    "@babel/plugin-transform-runtime": "^7.15.0",
    "@babel/preset-env": "^7.15.0",
    "@babel/runtime": "^7.15.3",
    "babel-loader": "^8.2.2",
    "css-loader": "^6.2.0",
    "html-webpack-plugin": "^5.3.2",
    "http-server": "^0.11.1",
    "style-loader": "^3.2.1",
    "webpack": "^5.51.1",
    "webpack-cli": "^4.8.0",
    "webpack-dev-server": "^4.0.0",
    "webpack-pwa-manifest": "^4.3.0",
    "workbox-webpack-plugin": "^6.2.4"
  },
  "dependencies": {
    "code-mirror-themes": "^1.0.0",
    "idb": "^6.1.2"
  }
}

```
Ensure the package.json in the root has the below scripts
```
{
"scripts": {
    "start:dev": "concurrently \"cd client && npm run build\" \"cd server && npm run server\" ",
    "start": "npm run build && cd server && node server.js",
    "server": "cd server nodemon server.js --ignore clien",
    "build": "cd client && npm run build",
    "install": "cd client && npm install",
    "client": "cd client && npm start"
  },
}
```
Run the below commands to install dependencies after cloning the repo
```
npm i
```

## Usage

* Ensure all depencies and above steps are fulfilled 
* Navigate to the working directory and open a terminal and run the below command
```
npm run start
```


## License

MIT License

Copyright (c) 2022 Siddharth Desai

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Tests

N/A

## Screenshots


![](./Assets/jate.gif)
![](./Assets/Capture.PNG)



## Questions?

Want to see more of my work? [Github Link](https://github.com/SHD327)
<br/>
Want to learn more please contact me at shdesai327@gmail.com


## Links

* [Github Link](https://github.com/shd327/Text-Editor)
* [Heroku Link](https://fast-woodland-35648.herokuapp.com/) 

## Resources

* https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps
* https://developers.google.com/web/tools/lighthouse
