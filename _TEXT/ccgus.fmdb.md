fmdb v2 7 a href http cocoadocs org docsets alamofire klzzwxh 0000 a this is an objective c wrapper around sqlite http sqlite org the fmdb mailing list http groups google com group fmdb read the sqlite faq http www sqlite org faq html since fmdb is built on top of sqlite youre going to want to read this page top to bottom at least once and while youre there make sure to bookmark the sqlite documentation page http www sqlite org docs html contributing do you have an awesome idea that deserves to be in fmdb you might consider pinging ccgus first to make sure he hasnt already ruled it out for some reason otherwise pull requests are great and make sure you stick to the local coding conventions however please be patient and if you havent heard anything from ccgus for a week or more you might want to send a note asking whats up installing cocoapods fmdb can be installed using cocoapods if you havent done so already you might want to initialize the project to have it produce a podfile template for you pod init then edit the podfile adding fmdb ruby uncomment the next line to define a global platform for your project platform ios 9 0 target myapp do comment the next line if youre not using swift and dont want to use dynamic frameworks use frameworks pods for myapp2 pod fmdb pod fmdb fts fmdb with fts pod fmdb standalone fmdb with latest sqlite amalgamation source pod fmdb standalone fts fmdb with latest sqlite amalgamation source and fts pod fmdb sqlcipher fmdb with sqlcipher end then install the pods pod install then open the xcworkspace rather than the xcodeproj for more information on cocoapods visit https cocoapods org if using fmdb with sqlcipher you must use the fmdb sqlcipher subspec the fmdb sqlcipher subspec declares sqlcipher as a dependency allowing fmdb to be compiled with the dsqlite has codec flag carthage once you make sure you have the latest version of carthage you can open up a command line terminal navigate to your projects main directory and then do the following commands echo github ccgus fmdb cartfile carthage update you can then configure your project as outlined in carthages getting started i e for ios adding the framework to the link binary with libraries in your target and adding the copy frameworks script in macos adding the framework to the list of embedded binaries fmdb class reference http ccgus github io fmdb html index html automatic reference counting arc or manual memory management you can use either style in your cocoa project fmdb will figure out which you are using at compile time and do the right thing whats new in fmdb 2 7 fmdb 2 7 attempts to support a more natural interface this represents a fairly significant change for swift developers audited for nullability shifted to properties in external interfaces where possible rather than methods etc for objective c developers this should be a fairly seamless transition unless you were using the ivars that were previously exposed in the public interface which you shouldnt have been doing anyway nullability and swift optionals fmdb 2 7 is largely the same as prior versions but has been audited for nullability for objective c users this simply means that if you perform a static analysis of your fmdb based project you may receive more meaningful warnings as you review your project but there are likely to be few if any changes necessary in your code for swift users this nullability audit results in changes that are not entirely backward compatible with fmdb 2 6 but is a little more swifty before fmdb was audited for nullability swift was forced to defensively assume that variables were optional but the library now more accurately knows which properties and method parameters are optional and which are not this means though that swift code written for fmdb 2 7 may require changes for example consider the following swift 3 swift 4 code for fmdb 2 6 swift queue intransaction db rollback in do guard let db db else handle error here return try db executeupdate insert into foo bar values values 1 try db executeupdate insert into foo bar values values 2 catch rollback pointee true because fmdb 2 6 was not audited for nullability swift inferred that db and rollback were optionals but now in fmdb 2 7 swift now knows that for example neither db nor rollback above can be nil so they are no longer optionals thus it becomes swift queue intransaction db rollback in do try db executeupdate insert into foo bar values values 1 try db executeupdate insert into foo bar values values 2 catch rollback pointee true custom functions in the past when writing custom functions you would have to generally include your own autoreleasepool block to avoid problems when writing functions that scanned through a large table now fmdb will automatically wrap it in an autorelease pool so you dont have to also in the past when retrieving the values passed to the function you had to drop down to the sqlite c api and include your own sqlite3 value xxx calls there are now fmdatabase methods valueint valuestring etc so you can stay within swift and or objective c without needing to call the c functions yourself likewise when specifying the return values you no longer need to call sqlite3 result xxx c api but rather you can use fmdatabase methods resultint resultstring etc there is a new enum for valuetype called sqlitevaluetype which can be used for checking the type of parameter passed to the custom function thus you can do something like as of swift 3 swift db makefunctionnamed removediacritics arguments 1 context argc argv in guard db valuetype argv 0 text db valuetype argv 0 null else db resulterror expected string parameter context context return if let string db valuestring argv 0 folding options diacriticinsensitive locale nil db resultstring string context context else db resultnull context context and you can then use that function in your sql in this case matching both jose and josé sql select from employees where removediacritics first name like jose note the method makefunctionnamed maximumarguments withblock has been renamed to makefunctionnamed arguments block to more accurately reflect the functional intent of the second parameter api changes in addition to the makefunctionnamed noted above there are a few other api changes specifically to become consistent with the rest of the api the methods objectforcolumnname and utf8stringforcolumnname have been renamed to objectforcolumn and utf8stringforcolumn note the objectforcolumn and the associted subscript operator now returns nil if an invalid column name index is passed to it it used to return nsnull to avoid confusion with fmdatabasequeue method intransaction which performs transactions the fmdatabase method to determine whether you are in a transaction or not intransaction has been replaced with a read only property isintransaction several functions have been converted to properties namely databasepath maxbusyretrytimeinterval shouldcachestatements sqlitehandle hasopenresultsets lastinsertrowid changes goodconnection columncount resultdictionary applicationid applicationidstring userversion countofcheckedindatabases countofcheckedoutdatabases and countofopendatabases for objective c users this has little material impact but for swift users it results in a slightly more natural interface note for objective c developers previously versions of fmdb exposed many ivars but we hope you werent using them directly anyway but the implmentation details for these are no longer exposed url methods in keeping with apples shift from paths to urls there are now nsurl renditions of the various init methods previously only accepting paths usage there are three main classes in fmdb fmdatabase represents a single sqlite database used for executing sql statements fmresultset represents the results of executing a query on an fmdatabase fmdatabasequeue if youre wanting to perform queries and updates on multiple threads youll want to use this class its described in the thread safety section below database creation an fmdatabase is created with a path to a sqlite database file this path can be one of these three a file system path the file does not have to exist on disk if it does not exist it is created for you an empty string an empty database is created at a temporary location this database is deleted when the fmdatabase connection is closed null an in memory database is created this database will be destroyed when the fmdatabase connection is closed for more information on temporary and in memory databases read the sqlite documentation on the subject http www sqlite org inmemorydb html objc nsstring path nstemporarydirectory stringbyappendingpathcomponent tmp db fmdatabase db fmdatabase databasewithpath path opening before you can interact with the database it must be opened opening fails if there are insufficient resources or permissions to open and or create the database objc if db open db release uncomment this line in manual referencing code in arc this is not necessary permitted db nil return executing updates any sort of sql statement which is not a select statement qualifies as an update this includes create update insert alter commit begin detach delete drop end explain vacuum and replace statements plus many more basically if your sql statement does not begin with select it is an update statement executing updates returns a single value a bool a return value of yes means the update was successfully executed and a return value of no means that some error was encountered you may invoke the lasterrormessage and lasterrorcode methods to retrieve more information executing queries a select statement is a query and is executed via one of the executequery methods executing queries returns an fmresultset object if successful and nil upon failure you should use the lasterrormessage and lasterrorcode methods to determine why a query failed in order to iterate through the results of your query you use a while loop you also need to step from one record to the other with fmdb the easiest way to do that is like this objc fmresultset s db executequery select from mytable while s next retrieve values for each record you must always invoke fmresultset next before attempting to access the values returned in a query even if youre only expecting one objc fmresultset s db executequery select count from mytable if s next int totalcount s intforcolumnindex 0 fmresultset has many methods to retrieve data in an appropriate format intforcolumn longforcolumn longlongintforcolumn boolforcolumn doubleforcolumn stringforcolumn dateforcolumn dataforcolumn datanocopyforcolumn utf8stringforcolumn objectforcolumn each of these methods also has a type forcolumnindex variant that is used to retrieve the data based on the position of the column in the results as opposed to the columns name typically theres no need to close an fmresultset yourself since that happens when either the result set is deallocated or the parent database is closed closing when you have finished executing queries and updates on the database you should close the fmdatabase connection so that sqlite will relinquish any resources it has acquired during the course of its operation objc db close transactions fmdatabase can begin and commit a transaction by invoking one of the appropriate methods or executing a begin end transaction statement multiple statements and batch stuff you can use fmdatabases executestatements withresultblock to do multiple statements in a string objc nsstring sql create table bulktest1 id integer primary key autoincrement x text create table bulktest2 id integer primary key autoincrement y text create table bulktest3 id integer primary key autoincrement z text insert into bulktest1 x values xxx insert into bulktest2 y values yyy insert into bulktest3 z values zzz success db executestatements sql sql select count as count from bulktest1 select count as count from bulktest2 select count as count from bulktest3 success self db executestatements sql withresultblock int nsdictionary dictionary nsinteger count dictionary count integervalue xctassertequal count 1 expected one record for dictionary dictionary return 0 data sanitization when providing a sql statement to fmdb you should not attempt to sanitize any values before insertion instead you should use the standard sqlite binding syntax sql insert into mytable values the character is recognized by sqlite as a placeholder for a value to be inserted the execution methods all accept a variable number of arguments or a representation of those arguments such as an nsarray nsdictionary or a va list which are properly escaped for you and to use that sql with the placeholders from objective c objc nsinteger identifier 42 nsstring name liam oflaherty \ the famous irish author\ nsdate date nsdate date nsstring comment nil bool success db executeupdate insert into authors identifier name date comment values identifier name date comment nsnull null if success nslog error db lasterrormessage note fundamental data types like the nsinteger variable identifier should be as a nsnumber objects achieved by using the syntax shown above or you can use the nsnumber numberwithint identifier syntax too likewise sql null values should be inserted as nsnull null for example in the case of comment which might be nil and is in this example you can use the comment nsnull null syntax which will insert the string if comment is not nil but will insert nsnull null if it is nil in swift you would use executeupdate values which not only is a concise swift syntax but also throws errors for proper error handling swift do let identifier 42 let name liam oflaherty \ the famous irish author\ let date date let comment string nil try db executeupdate insert into authors identifier name date comment values values identifier name date comment nsnull catch print error error note in swift you dont have to wrap fundamental numeric types like you do in objective c but if you are going to insert an optional string you would probably use the comment nsnull syntax i e if it is nil use nsnull otherwise use the string alternatively you may use named parameters syntax sql insert into authors identifier name date comment values identifier name date comment the parameters must start with a colon sqlite itself supports other characters but internally the dictionary keys are prefixed with a colon do not include the colon in your dictionary keys objc nsdictionary arguments identifier identifier name name date date comment comment nsnull null bool success db executeupdate insert into authors identifier name date comment values identifier name date comment withparameterdictionary arguments if success nslog error db lasterrormessage the key point is that one should not use nsstring method stringwithformat to manually insert values into the sql statement itself nor should one swift string interpolation to insert values into the sql use placeholders for values to be inserted into the database or used in where clauses in select statements using fmdatabasequeue and thread safety using a single instance of fmdatabase from multiple threads at once is a bad idea it has always been ok to make a fmdatabase object per thread just dont share a single instance across threads and definitely not across multiple threads at the same time bad things will eventually happen and youll eventually get something to crash or maybe get an exception or maybe meteorites will fall out of the sky and hit your mac pro this would suck so dont instantiate a single fmdatabase object and use it across multiple threads instead use fmdatabasequeue instantiate a single fmdatabasequeue and use it across multiple threads the fmdatabasequeue object will synchronize and coordinate access across the multiple threads heres how to use it first make your queue objc fmdatabasequeue queue fmdatabasequeue databasequeuewithpath apath then use it like so objc queue indatabase fmdatabase db db executeupdate insert into mytable values 1 db executeupdate insert into mytable values 2 db executeupdate insert into mytable values 3 fmresultset rs db executequery select from foo while rs next … an easy way to wrap things up in a transaction can be done like this objc queue intransaction fmdatabase db bool rollback db executeupdate insert into mytable values 1 db executeupdate insert into mytable values 2 db executeupdate insert into mytable values 3 if whoopssomethingwronghappened rollback yes return etc the swift equivalent would be swift queue intransaction db rollback in do try db executeupdate insert into mytable values values 1 try db executeupdate insert into mytable values values 2 try db executeupdate insert into mytable values values 3 if whoopssomethingwronghappened rollback pointee true return etc catch rollback pointee true print error note as of swift 3 use pointee but in swift 2 3 use memory rather than pointee fmdatabasequeue will run the blocks on a serialized queue hence the name of the class so if you call fmdatabasequeues methods from multiple threads at the same time they will be executed in the order they are received this way queries and updates wont step on each others toes and every one is happy note the calls to fmdatabasequeues methods are blocking so even though you are passing along blocks they will not be run on another thread making custom sqlite functions based on blocks you can do this for an example look for makefunctionnamed in main m swift you can use fmdb in swift projects too to do this you must copy the relevant m and h files from the fmdb src folder into your project you can copy all of them which is easiest or only the ones you need likely you will need fmdatabase and fmresultset at a minimum fmdatabaseadditions provides some very useful convenience methods so you will likely want that too if you are doing multithreaded access to a database fmdatabasequeue is quite useful too if you choose to not copy all of the files from the src directory though you may want to update fmdb h to only reference the files that you included in your project note if youre copying all of the files from the src folder into to your project which is recommended you may want to drag the individual files into your project not the folder itself because if you drag the folder you wont be prompted to add the bridging header see next point if prompted to create a bridging header you should do so if not prompted and if you dont already have a bridging header add one for more information on bridging headers see swift and objective c in the same project in your bridging header add a line that says objc import fmdb h use the variations of executequery and executeupdate with the sql and values parameters with try pattern as shown below these renditions of executequery and executeupdate both throw errors in true swift fashion if you do the above you can then write swift code that uses fmdatabase for example as of swift 3 swift let fileurl try filemanager default url for applicationsupportdirectory in userdomainmask appropriatefor nil create true appendingpathcomponent test sqlite let database fmdatabase url fileurl guard database open else print unable to open database return do try database executeupdate create table test x text y text z text values nil try database executeupdate insert into test x y z values values a b c try database executeupdate insert into test x y z values values e f g let rs try database executequery select x y z from test values nil while rs next if let x rs string forcolumn x let y rs string forcolumn y let z rs string forcolumn z print x \ x y \ y z \ z catch print failed error localizeddescription database close history the history and changes are availbe on its github page and are summarized in the changes and todo list txt file contributors the contributors to fmdb are contained in the contributors txt file additional projects using fmdb which might be interesting to the discerning developer fmdbmigrationmanager a sqlite schema migration management system for fmdb https github com layerhq fmdbmigrationmanager fcmodel an alternative to core data for people who like having direct sql access https github com marcoarment fcmodel quick notes on fmdbs coding style spaces not tabs square brackets not dot notation look at what fmdb already does with curly brackets and such and stick to that style reporting bugs reduce your bug down to the smallest amount of code possible you want to make it super easy for the developers to see and reproduce your bug if it helps pretend that the person who can fix your bug is active on shipping 3 major products works on a handful of open source projects has a newborn baby and is generally very very busy and weve even added a template function to main m fmdbreportabugfunction in the fmdb distribution to help you out open up fmdb project in xcode open up main m and modify the fmdbreportabugfunction to reproduce your bug setup your table s in the code make your query or update s add some assertions which demonstrate the bug then you can bring it up on the fmdb mailing list by showing your nice and compact fmdbreportabugfunction or you can report the bug via the github fmdb bug reporter optional figure out where the bug is fix it and send a patch in or bring that up on the mailing list make sure all the other tests run after your modifications support the support channels for fmdb are the mailing list see above filing a bug here or maybe on stack overflow so that is to say support is provided by the community and on a voluntary basis fmdb development is overseen by gus mueller of flying meat if fmdb been helpful to you consider purchasing an app from fm or telling all your friends about it license the license for fmdb is contained in the license txt file if you happen to come across either gus mueller or rob ryan in a bar you might consider purchasing a drink of their choosing if fmdb has been useful to you the drink is for them of course shame on you for trying to keep it