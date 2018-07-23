monolog logging for php monolog sends your logs to files sockets inboxes databases and various web services see the complete list of handlers below special handlers allow you to build advanced logging strategies this library implements the psr 3 interface that you can type hint against in your own libraries to keep a maximum of interoperability you can also use it in your applications to make sure you can always use another compatible logger at a later time as of 1 11 0 monolog public apis will also accept psr 3 log levels internally monolog still uses its own level scheme since it predates psr 3 installation install the latest version with bash composer require monolog monolog basic usage php php use monolog\logger use monolog\handler\streamhandler create a log channel log new logger name log pushhandler new streamhandler path to your log logger warning add records to the log log warning foo log error bar documentation usage instructions handlers formatters and processors utility classes extending monolog log record structure third party packages third party handlers formatters and processors are listed in the wiki you can also add your own there if you publish one about requirements monolog 2 x works with php 7 1 or above use monolog 1 0 for php 5 3 support submitting bugs and feature requests bugs and feature request are tracked on github framework integrations frameworks and libraries using psr 3 can be used very easily with monolog since it implements the interface symfony2 comes out of the box with monolog silex comes out of the box with monolog laravel 4 5 come out of the box with monolog lumen comes out of the box with monolog ppi comes out of the box with monolog cakephp is usable with monolog via the cakephp monolog plugin slim is usable with monolog via the slim monolog log writer xoops 2 6 comes out of the box with monolog aura web project comes out of the box with monolog nette framework can be used with monolog via kdyby monolog extension proton micro framework comes out of the box with monolog fuelphp comes out of the box with monolog equip framework comes out of the box with monolog yii 2 is usable with monolog via the yii2 monolog or yii2 psr log target plugins hawkbit micro framework comes out of the box with monolog author jordi boggiano j boggiano seld be http twitter com seldaek see also the list of contributors which participated in this project license monolog is licensed under the mit license see the license file for details acknowledgements this library is heavily inspired by pythons logbook library although most concepts have been adjusted to fit to the php world