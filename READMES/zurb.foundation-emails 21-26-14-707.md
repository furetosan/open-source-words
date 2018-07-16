foundation for emails foundation for emails previously known as ink is a framework for creating responsive html emails that work in any email client — even outlook our html css components have been tested across every major email client to ensure consistency and with the inky templating language writing html emails is now even easier getting started the main way to get started is with our email template stack to use the stack youll need node js installed on your machine to set up the emails template run these commands bash git clone https github com zurb foundation emails template project cd project npm install then run npm start to run the project a new browser window will open with a browsersync server showing the finished files run npm run build to do a full email inlining process using the ruby gem foundation emails is a gem that enables you to use foundation for emails assets within a rails project to install in your app add the following line to your gemfile ruby gem foundation emails then execute bash bundle install import foundation for emails in your emails stylesheet s scss app assets stylesheets your emails stylesheet scss import foundation emails adding inkys templating capabilities to rails is easy thanks to the inky rb gem which bundles foundation emails by default documentation check out our migration guide for upgrading an existing template or for more in depth code examples foundation for emails 2 0 documentation and framework are on the develop branch and you can compile it on your own machine run these commands to set up the documentation bash git clone https github com zurb foundation emails git cd foundation emails foundation for emails 2 0 documentation is on the develop branch bash git fetch git checkout develop npm install then run npm start to compile the documentation when it finishes a new browser window will open pointing to a browsersync server displaying the documentation testing run npm run test visual to compile the visual regression tests all of the pages under test visual pages are compiled and inlined from there they can be uploaded to litmus for testing inky inky is our new templating language that converts simple html into the complex tables required for email layout the parser converts a set of custom html tags expanding them out into full html syntax below is a list of every custom element grid html container row column small 12 large 4 column column small 12 large 8 column row container block grid html block grid up 3 td td td td td td block grid components html button href http zurb com button html menu item href one html item one item item href one html item two item item href one html item three item menu contributing as an open source project we looooove our community support please file issues or better yet pull requests on the foundation for emails repo were stoked to hear your feedback make improvements and keep evolving foundation for emails copyright c 2018 zurb inc