vue webpack boilerplate a full featured webpack setup with hot reload lint on save unit testing css extraction this template is vue 2 0 compatible for vue 1 x use this command vue init webpack 1 0 my project documentation for this template common questions specific to this template are answered and each part is described in greater detail for vue 2 0 general information about how to work with vue not specific to this template usage this is a project template for vue cli it is recommended to use npm 3 for a more efficient dependency tree bash npm install g vue cli vue init webpack my project cd my project npm install npm run dev this will scaffold the project using the master branch if you wish to use the latest version of the webpack template do the following instead bash vue init webpack develop my project warning the develop branch is not considered stable and can contain bugs or not build at all so use at your own risk the development server will run on port 8080 by default if that port is already in use on your machine the next free port will be used whats included npm run dev first in class development experience webpack vue loader for single file vue components state preserving hot reload state preserving compilation error overlay lint on save with eslint source maps npm run build production ready build javascript minified with uglifyjs v3 html minified with html minifier css across all components extracted into a single file and minified with cssnano static assets compiled with version hashes for efficient long term caching and an auto generated production index html with proper urls to these generated assets use npm run build reportto build with bundle size analytics npm run unit unit tests run in jsdom with jest or in phantomjs with karma mocha karma webpack supports es2015 in test files easy mocking npm run e2e end to end tests with nightwatch run tests in multiple browsers in parallel works with one command out of the box selenium and chromedriver dependencies automatically handled automatically spawns the selenium server fork it and make your own you can fork this repo to create your own boilerplate and use it with vue cli bash vue init username repo my project