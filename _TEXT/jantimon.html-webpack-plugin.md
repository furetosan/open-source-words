html webpack plugin plugin that simplifies creation of html files to serve your bundles install alpha bash npm i save dev html webpack plugin next bash yarn add dev html webpack plugin next install stable bash npm i save dev html webpack plugin bash yarn add dev html webpack plugin this is a webpack plugin that simplifies creation of html files to serve your webpack bundles this is especially useful for webpack bundles that include a hash in the filename which changes every compilation you can either let the plugin generate an html file for you supply your own template using lodash templates or use your own loader plugins the html webpack plugin provides hooks to extend it to your needs there are already some really powerful plugins which can be integrated with zero configuration webpack subresource integrity for enhanced asset security appcache webpack plugin for ios and android offline usage favicons webpack plugin which generates favicons and icons for ios android and desktop browsers html webpack harddisk plugin can be used to always write to disk the html file useful when webpack dev server hmr are being used html webpack inline source plugin to inline your assets in the resulting html file html webpack inline svg plugin to inline svgs in the resulting html file html webpack exclude assets plugin for excluding assets using regular expressions html webpack include assets plugin for including lists of js or css file paths such as those copied by the copy webpack plugin script ext html webpack plugin to add async defer or module attributes to your script elements or even inline them style ext html webpack plugin to convert your link s to external stylesheets into style elements containing internal css resource hints webpack plugin to add resource hints for faster initial page loads using link rel preload and link rel prefetch preload webpack plugin for automatically wiring up asynchronous and other types of javascript chunks using link rel preload helping with lazy loading link media html webpack plugin allows for injected stylesheet link tags to have their media attribute set automatically useful for providing specific desktop mobile print etc stylesheets that the browser will conditionally download inline chunk manifest html webpack plugin for inlining webpacks chunk manifest default extracts manifest and inlines in head html webpack inline style plugin for inlining styles to html elements using juice useful for email generation automatisation html webpack exclude empty assets plugin removes empty assets from being added to the html this fixes some problems with extract text plugin with webpack 4 webpack concat plugin for concat and uglify files that neednt to be webpack bundles for legacy files and inject to html webpack plugin usage the plugin will generate an html5 file for you that includes all your webpack bundles in the body using script tags just add the plugin to your webpack config as follows webpack config js js const htmlwebpackplugin require html webpack plugin module exports entry index js output path dirname dist filename index bundle js plugins new htmlwebpackplugin this will generate a file dist index html containing the following html doctype html html head meta charset utf 8 title webpack app title head body script src index bundle js script body html if you have multiple webpack entry points they will all be included with script tags in the generated html if you have any css assets in webpacks output for example css extracted with the extracttextplugin then these will be included with link tags in the html head if you have plugins that make use of it html webpack plugin should be ordered first before any of the integrated plugins options you can pass a hash of configuration options to html webpack plugin allowed values are as follows name type default description title string webpack app the title to use for the generated html document filename string index html the file to write the html to defaults to index html you can specify a subdirectory here too eg assets admin html template string webpack require path to the template please see the docs https github com jantimon html webpack plugin blob master docs template option md for details templateparameters boolean\ object\ function allows to overwrite the parameters used in the template inject boolean\ string true true \ \ head \ \ body \ \ false inject all assets into the given template or templatecontent when passing true or body all javascript resources will be placed at the bottom of the body element head will place the scripts in the head element favicon string adds the given favicon path to the output html meta object allows to inject meta tags e g meta viewport width device width initial scale 1 shrink to fit no minify boolean\ object false pass html minifier https github com kangax html minifier options quick reference s options as object to minify the output hash boolean false if true then append a unique webpack compilation hash to all included scripts and css files this is useful for cache busting cache boolean true emit the file only if it was changed showerrors boolean true errors details will be written into the html page chunks allows you to add only some chunks e g only the unit test chunk chunkssortmode plugins string\ function auto allows to control how chunks should be sorted before they are included to the html allowed values are none \ auto \ dependency \ manual \ function excludechunks array string allows you to skip some chunks e g dont add the unit test chunk xhtml boolean false if true render the link tags as self closing xhtml compliant heres an example webpack config illustrating how to use these options webpack config js js entry index js output path dirname dist filename index bundle js plugins new htmlwebpackplugin title my app filename assets admin html generating multiple html files to generate more than one html file declare the plugin more than once in your plugins array webpack config js js entry index js output path dirname dist filename index bundle js plugins new htmlwebpackplugin generates default index html new htmlwebpackplugin also generate a test html filename test html template src assets test html writing your own templates if the default generated html doesnt meet your needs you can supply your own template the easiest way is to use the template option and pass a custom html file the html webpack plugin will automatically inject all necessary css js manifest and favicon files into the markup js plugins new htmlwebpackplugin title custom template load a custom template lodash by default see the faq for details template index html index html html doctype html html head meta http equiv content type content text html charset utf 8 title htmlwebpackplugin options title title head body body html if you already have a template loader you can use it to parse the template please note that this will also happen if you specifiy the html loader and use html file as template webpack config js js module loaders test \ hbs loader handlebars loader plugins new htmlwebpackplugin title custom template using handlebars template index hbs you can use the lodash syntax out of the box if the inject feature doesnt fit your needs and you want full control over the asset placement use the default template of the html webpack template project as a starting point for writing your own the following variables are available in the template htmlwebpackplugin data specific to this plugin htmlwebpackplugin files a massaged representation of the assetsbychunkname attribute of webpacks stats object it contains a mapping from entry point name to the bundle filename eg json htmlwebpackplugin files css main css js assets head bundle js assets main bundle js chunks head entry assets head bundle js css main css main entry assets main bundle js css if youve set a publicpath in your webpack config this will be reflected correctly in this assets hash htmlwebpackplugin options the options hash that was passed to the plugin in addition to the options actually used by this plugin you can use this hash to pass arbitrary data through to your template webpack the webpack stats object note that this is the stats object as it was at the time the html template was emitted and as such may not have the full set of stats that are available after the webpack run is complete webpackconfig the webpack configuration that was used for this compilation this can be used for example to get the publicpath webpackconfig output publicpath compilation the webpack compilation object this can be used for example to get the contents of processed assets and inline them directly in the page through compilation assets source see the inline template example filtering chunks to include only certain chunks you can limit the chunks being used webpack config js js plugins new htmlwebpackplugin chunks app it is also possible to exclude certain chunks by setting the excludechunks option webpack config js js plugins new htmlwebpackplugin excludechunks dev helper events to allow other plugins to alter the html this plugin executes the following events syncwaterfallhook htmlwebpackpluginalterchunks asyncserieswaterfallhook htmlwebpackpluginbeforehtmlgeneration htmlwebpackpluginbeforehtmlprocessing htmlwebpackpluginalterassettags htmlwebpackpluginafterhtmlprocessing htmlwebpackpluginafteremit example implementation html webpack harddisk plugin plugin js js function myplugin options configure your plugin with options myplugin prototype apply function compiler compiler hooks compilation tap myplugin compilation console log the compiler is starting a new compilation compilation hooks htmlwebpackpluginafterhtmlprocessing tapasync myplugin data cb data html the magic footer cb null data module exports myplugin webpack config js js plugins new myplugin options note that the callback must be passed the htmlwebpackplugindata in order to pass this onto any other plugins listening on the same html webpack plugin before html processing event maintainers jan nicklas thomas sileghem contributors this project exists thanks to all the people who contribute youre free to contribute to this project by submitting issues and or pull requests this project is test driven so keep in mind that every change and new feature should be covered by tests this project uses the semistandard code style backers thank you to all our backers 🙏 become a backer sponsors support this project by becoming a sponsor your logo will show up here with a link to your website become a sponsor