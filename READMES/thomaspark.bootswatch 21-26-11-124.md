bootswatch bootswatch is a collection of open source themes for bootstrap check it out at bootswatch com usage there are a few different ways you can integrate bootswatch into your project via pre compiled asset download the bootstrap min css file associated with a theme and replace bootstraps default stylesheet you must still include bootstraps javascript file to have functional dropdowns modals etc via cdn similar to above but you can hotlink to the appropriate bootstrap min css hosted on bootstrapcdn via sass imports if youre using sass scss in your project you can import the variables scss and bootswatch scss files for a given theme this method allows you to override theme variables scss your variable overrides go here e g h1 font size 3rem import bootswatch dist theme variables import bootstrap scss bootstrap import bootswatch dist theme bootswatch make sure to import bootstraps bootstrap scss in between variables scss and bootswatch scss via npm you can install as a package with the command npm install bootswatch via ruby gem in your ruby project you can access the latest version of each theme by adding the following to your gemfile and running bundle install ruby gem bootswatch github thomaspark bootswatch each theme directory is then accessible via the path gem loaded specs bootswatch load paths first theme ruby on rails users can add the following to an initializer e g config initializers bootswatch rb ruby rails application config assets paths gem loaded specs bootswatch load paths and thus be able to import themes via sass like so scss import theme variables import bootstrap scss bootstrap import theme bootswatch via api a simple json api is available for integrating your platform with bootswatch more info can be found on the help page customization bootswatch is open source and youre welcome to modify the themes each theme consists of two sass files variables scss which is included by default in bootstrap allows you to customize the settings bootswatch scss introduces more extensive structural changes check out the help page for more details on building your own theme contributing its through your contributions that bootswatch will continue to improve you can contribute in several ways issues provide a detailed report of any bugs you encounter and open an issue on github documentation if youd like to fix a typo or beef up the docs you can fork the project make your changes and submit a pull request code make a fix and submit it as a pull request when making changes its important to keep the css and sass versions in sync to do this be sure to edit the sass source files for the particular theme first then run the tasks grunt swatch to build the css donation donations are gratefully accepted via paypal and bitcoin at 1emqwwjqjrfyopqmxnm7buzu6dmysznhbk author thomas park https github com thomaspark https thomaspark co thanks mark otto and jacob thornton for bootstrap jenil gogari for his contributions to the flatly theme james taylor for cors lite corey sewell for sass conversion copyright and license copyright 2014 2018 thomas park code released under the mit license