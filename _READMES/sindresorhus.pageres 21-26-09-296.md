capture screenshots of websites in various resolutions a good way to make sure your websites are responsive its speedy and generates 100 screenshots from 10 different websites in just over a minute it can also be used to render svg images see pageres cli for the command line tool install npm install pageres phantomjs which is used for generating the screenshots is installed automagically but in some rare cases it might fail to and youll get an error spawn eacces error download phantomjs manually and reinstall pageres if that happens usage js const pageres require pageres const pageres new pageres delay 2 src yeoman io 480x320 1024x768 iphone 5s crop true src todomvc com 1280x1024 1920x1080 src data text html base64 pggxpkzptzwvade 1024x768 dest dirname run then console log done api pageres options options delay type number seconds default 0 delay capturing the screenshot useful when the site does things after load that you want to capture timeout type number seconds default 60 number of seconds after which phantomjs aborts the request crop type boolean default false crop to the set height css type string apply custom css to the webpage specify some css or the path to a css file script type string apply custom javascript to the webpage specify some javascript or the path to a file cookies type array string object a string with the same format as a browser cookie or an object of what phantomjs addcookie accepts tip go to the website you want a cookie for and copy paste it from dev tools filename type string define a customized filename using lo dash templates for example date url size crop available variables url the url in slugified form eg http yeoman io blog becomes yeoman io blog size specified size eg 1024x1000 width width of the specified size eg 1024 height height of the specified size eg 1000 crop outputs cropped when the crop option is true date the current date y m d eg 2015 05 18 time the current time h m s eg 21 15 11 incrementalname type boolean default false when a file exists append an incremental number selector type string capture a specific dom element matching a css selector hide type array string hide an array of dom elements matching css selectors username type string username for authenticating with http auth password type string password for authenticating with http auth scale type number default 1 scale webpage n times format type string default png values png jpg image format useragent type string custom user agent headers type object custom http request headers transparent type boolean default false set background color to transparent instead of white if no background is set pageres src url sizes options add a page to screenshot url required type string url or local path to the website you want to screenshot you can also use a data uri sizes required type array string use a width x height notation or a keyword a keyword is a version of a device from this list you can also pass in the w3counter keyword to use the ten most popular resolutions from w3counter options type object options set here will take precedence over the ones set in the constructor pageres dest directory set the destination directory directory type string pageres run run pageres returns a promise for an array of streams pageres on warning callback warnings with e g page errors task runners check out grunt pageres if youre using grunt for gulp and broccoli just use the api directly no need for a wrapper plugin built with pageres break shot desktop app for capturing screenshots of responsive websites team sindre sorhus kevin mårtensson sam verschueren license mit © sindre sorhus