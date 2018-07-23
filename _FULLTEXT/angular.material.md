Material Design for AngularJS Apps Material Design is a specification for a unified system of visual, motion, and interaction design that adapts across different devices. Our goal is to deliver a lean, lightweight set of AngularJS-native UI elements that implement the material design specification for use in AngularJS single-page applications (SPAs). AngularJS Material is an implementation of Googles Material Design Specification. AngularJS Material includes a rich set of reusable, well-tested, and accessible UI components. Quick Links: API & Demos Contributing Building Installing Please note that using AngularJS Material requires the use of AngularJS 1.4.x or higher. AngularJS Material is targeted for the browser versions defined in the broswerslist field of our package.json. Below is a screenshot from browserl.ist that provides a visual representation of this configuration: Online Documentation and Demos Visit material.angularjs.org online to review the API, see the components in action via live demos, and to read our detailed guides which include the layout system, theming system, typography, and more. Or you can build the documentation and demos locally; see Build Docs & Demos for details. Our Release Processes To preserve stability with applications currently using AngularJS Material, we do not follow semver. We have three types of releases: major : major releases will be done in the separate Angular Material repo. This type of release will not be used within AngularJS Material. minor: contain breaking changes in addition to patch release changes. patch: non-breaking changes (no API, CSS, UX changes that will cause breaks in existing AngularJS Material applications). Patch Releases The patch builds (1.1.4, 1.1.5, 1.1.6) are prepared based on commits in the master branch; which contains only non-breaking changes (I.e. bug fixes, new features, API additions, and minimal non-breaking CSS changes). We are targeting patch releases every 2 weeks. Minor Releases The minor builds (1.1.0, 1.2.0, 1.3.0) can contain breaking changes to CSS, APIs, and UX. Our formal release of minor builds is much less frequent. The release process for minor builds is currently being re-evaluated. For the purposes of AngularJS Material, you could think of the patch releases as being minor changes and the minor releases as being major changes according to semver. Contributing Developers interested in contributing should read the following guidelines: Issue Guidelines Contributing Guidelines Coding Guidelines Pull Request Guide Software Process Change Log Please do not ask general questions in an issue. Issues are only to report bugs, request enhancements, or request new features. For general questions and discussions, use the AngularJS Material Forum. It is important to note that for each release, the ChangeLog is a resource that will itemize all: Bug Fixes New Features Breaking Changes Building Developers can build AngularJS Material using NPM and gulp. First install or update your local projects npm dependencies: bash npm install Then run the gulp tasks: ```bash To build angular-material.js/.css and Theme files in the /dist directory gulp build To build the AngularJS Material Docs and Demos in /dist/docs directory gulp docs ``` For development, use the docs:watch NPM script to run in dev mode: ```bash To build the AngularJS Material Source, Docs, and Demos in watch mode npm run docs:watch ``` For more details on how the build process works and additional commands (available for testing and debugging) developers should read the Build Guide. Installing Build (Distribution Files) NPM For developers not interested in building the AngularJS Material library... use NPM to install and use the AngularJS Material distribution files. Change to your projects root directory. ```bash To get the latest stable version, use Bower from the command line. npm install angular-material --save To get the most recent, latest committed-to-master version use: npm install http://github.com/angular/bower-material#master --save ``` Other Dependency Managers Visit Bower-Material for more details on how to install and use the AngularJS Material distribution files within your own local project. This includes instructions for Bower and JSPM. CDN CDN versions of AngularJS Material are now available. With the Google CDN, you will not need to download local copies of the distribution files. Instead simply reference the CDN urls to easily use those remote library files. This is especially useful when using online tools such as CodePen, Plunkr, or JSFiddle. ```html <!-- AngularJS Material CSS now available via Google CDN; version 1.1.9 used here --> <!-- AngularJS Material Dependencies --> <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.7/angular.min.js"></script> <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.7/angular-animate.min.js"></script> <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.7/angular-aria.min.js"></script> <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.7/angular-messages.min.js"></script> <!-- AngularJS Material Javascript now available via Google CDN; version 1.1.4 used here --> <script src="https://ajax.googleapis.com/ajax/libs/angular_material/1.1.9/angular-material.min.js"></script> ``` Developers seeking the latest, most-current build versions can use GitCDN.link to pull directly from the distribution GitHub Bower-Material repository: ```html <!-- AngularJS Material CSS using GitCDN to load directly from `bower-material/master` --> <link rel="stylesheet" href="https://cdn.gitcdn.link/cdn/angular/bower-material/master/angular-material.css"> <!-- AngularJS Material Dependencies --> <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.js"></script> <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular-animate.js"></script> <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular-aria.js"></script> <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular-messages.min.js"></script> <!-- AngularJS Material Javascript using GitCDN to load directly from `bower-material/master` --> <script src="https://cdn.gitcdn.link/cdn/angular/bower-material/master/angular-material.js"></script> ``` Once you have all the necessary assets installed, add ngMaterial and ngMessages as dependencies for your app: javascript angular.module(myApp, [ngMaterial, ngMessages]);