owl carousel 2 touch enabled jquery plugin that lets you create a beautiful responsive carousel slider to get started check out https owlcarousel2 github io owlcarousel2 notice the old owl carousel site owlgraphic dot com is no longer in use please delete all references to this in bookmarks and your own products documentation as its being used for malicious purposes quick start install this package can be installed with npm npm install save owl carousel or yarn add owl carousel jquery bower bower install save owl carousel or download the latest release load webpack add jquery via the webpack provideplugin to your webpack configuration const webpack require webpack plugins new webpack provideplugin jquery jquery jquery window jquery jquery load the required stylesheet and js js import owl carousel dist assets owl carousel css import owl carousel static html put the required stylesheet at the top of your markup html link rel stylesheet href node modules owl carousel dist assets owl carousel min css html link rel stylesheet href bower components owl carousel dist assets owl carousel min css note if you want to use the default navigation styles you will also need to include owl theme default css put the script at the bottom of your markup right after jquery html script src node modules jquery dist jquery js script script src node modules owl carousel dist owl carousel min js script html script src bower components jquery dist jquery js script script src bower components owl carousel dist owl carousel min js script usage wrap your items div a img span li etc with a container element div ul etc only the class owl carousel is mandatory to apply proper styles html div class owl carousel owl theme div your content div div your content div div your content div div your content div div your content div div your content div div your content div div note the owl theme class is optional but without it you will need to style navigation features on your own call the plugin function and your carousel is ready javascript document ready function owl carousel owlcarousel documentation the documentation included in this repo in the root directory is built with assemble and publicly available at https owlcarousel2 github io owlcarousel2 the documentation may also be run locally building this package comes with grunt and bower the following tasks are available default compiles the css and js into dist and builds the doc dist compiles the css and js into dist only watch watches source files and builds them automatically whenever you save test runs jshint and qunit tests headlessly in phantomjs to define which plugins are build into the distribution just edit config json to fit your needs contributing please read contributing md roadmap please make sure to check out our roadmap discussion license the code and the documentation are released under the mit license