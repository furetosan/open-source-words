whoops php errors for cool kids whoops is an error handler framework for php out of the box it provides a pretty error interface that helps you debug your web projects but at heart its a simple yet powerful stacked error handling system features flexible stack based error handling stand alone library with currently no required dependencies simple api for dealing with exceptions trace frames their data includes a pretty rad error page for your webapp projects includes the ability to open referenced files directly in your editor and ide includes handlers for different response formats json xml soap easy to extend and integrate with existing libraries clean well structured tested code base installing if you use laravel 4 or laravel 5 5 you already have whoops there are also community provided instructions on how to integrate whoops into silex 1 silex 2 phalcon laravel 3 laravel 5 cakephp 2 cakephp 3 zend 2 zend 3 yii 1 fuelphp slim pimple or any framework consuming stackphp middlewares or psr 7 middlewares if you are not using any of these frameworks heres a very simple way to install use composer to install whoops into your project bash composer require filp whoops register the pretty handler in your code php whoops new \whoops\run whoops pushhandler new \whoops\handler\prettypagehandler whoops register for more options have a look at the example files in examples to get a feel for how things work also take a look at the api documentation and the list of available handers below you may also want to override some system calls whoops does to do that extend whoops\util\systemfacade override functions that you want and pass it as the argument to the run constructor available handlers whoops currently ships with the following built in handlers available in the whoops\handler namespace prettypagehandler shows a pretty error page when something goes pants up plaintexthandler outputs plain text message for use in cli applications callbackhandler wraps a closure or other callable as a handler you do not need to use this handler explicitly whoops will automatically wrap any closure or callable you pass to whoops\run pushhandler jsonresponsehandler captures exceptions and returns information on them as a json string can be used to for example play nice with ajax requests xmlresponsehandler captures exceptions and returns information on them as a xml string can be used to for example play nice with ajax requests you can also use pluggable handlers such as soap handler authors this library was primarily developed by filipe dobreira and is currently maintained by denis sokolov a lot of awesome fixes and enhancements were also sent in by various contributors special thanks to graham campbell and markus staab for continuous participation this software includes prettify licensed under apache license 2 0 it is bundled only as a performance optimization