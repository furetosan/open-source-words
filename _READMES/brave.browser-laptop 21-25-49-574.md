brave browser desktop browser for macos windows and linux follow brave on twitter for important news and announcements for other versions of our browser please see iphone brave browser ios android brave browser android tabs downloads to download the latest release see our releases page you can also visit our website to get the latest stable release along with a more user friendly download page brave supports 4 release channels release beta developer and nightly community join the q a community if youd like to get more involved with brave you can ask for help discuss features youd like to see and a lot more wed love to have your help so that we can continue improving brave join our discord community chat for higher bandwidth discussions useful documentation see contributing md for tips and guidelines about contributing see docs style md for information on styling see docs tests md for information on testing including how to run a subset of the tests see docs debugging md for information on debugging see docs translations md to learn how you can help us with translations localization see docs linuxinstall md for information on installing the browser on linux distributions running from source if youre setting up using windows please see the building on windows wiki entry for a full walkthrough for other platforms macos linux youll need certain packages installed before you can build and run brave locally prerequisites the current lts version of nodejs install from your package manager nvm or download from https nodejs org npm version 5 or greater to make use of the package lock json on debian ubuntu mint apt get install build essential rpm ninja build on fedora dnf install rpm build dnf group install development tools c development tools and libraries on solus sudo eopkg it c system devel gconf installation after installing the prerequisites clone the git repository from github for beta testers git clone depth 1 https github com brave browser laptop for devs over https git clone https github com brave browser laptop for devs over ssh git clone git github com brave browser laptop git open the working directory cd browser laptop install the node dependencies npm install instead of npm install you may also install with yarn running yarn install troubleshooting additional notes on troubleshooting installation issues are in the troubleshooting page in the wiki preconfigured vms some platforms are available as pre configured vms see the readme for details running brave running a development version of the browser requires two steps the easiest way is just to use two terminals or one terminal with two tabs first youll need to start the watch process which runs webpack and watches for changes to the code npm run watch second you can start the actual brave process in another terminal or tab npm start some errors related to brave electron update can be fixed by doing a clean install rm rf node modules npm install if this does not work please clear out your electron first and try again running webdriver tests to run the webdriver tests npm run watch test or npm run watch all now run tests in another terminal npm test see docs tests md for more information port brave uses port 8080 to communicate between its client and server sides by default if you are using port 8080 for something else e g a web proxy then you can set the node config to make it use a different one e g npm config set brave port 9001 additional notes on troubleshooting development issues are in the troubleshooting page in the wiki running inside of a development version of muon by default we provide pre built binaries when you npm install with our own fork of electron prebuilt if you want to modify the code to muon braves electron fork then youll need to build it an example of why you might do that would be exposing a new event to the webview from muon to start this process youll want to check out our browser laptop bootstrap repo from there you can follow the steps in our wiki to get up and running packaging for bundles installers and updates please see our wiki entry for more information about packaging