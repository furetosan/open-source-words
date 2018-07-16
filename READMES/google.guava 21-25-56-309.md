guava google core libraries for java guava is a set of core libraries that includes new collection types such as multimap and multiset immutable collections a graph library functional types an in memory cache and apis utilities for concurrency i o hashing primitives reflection string processing and much more guava comes in two flavors the jre flavor requires jdk 1 8 or higher if you need support for jdk 1 7 or android use the android flavor you can find the android guava source in the android directory adding guava to your build guavas maven group id is com google guava and its artifact id is guava guava provides two different flavors one for use on a java 8 jre and one for use on android or java 7 or by any library that wants to be compatible with either of those these flavors are specified in the maven version field as either 25 1 jre or 25 1 android for more about depending on guava see using guava in your build to add a dependency on guava using maven use the following xml dependency groupid com google guava groupid artifactid guava artifactid version 25 1 jre version or for android version 25 1 android version dependency to add a dependency using gradle dependencies compile com google guava guava 25 1 jre or for android api com google guava guava 25 1 android snapshots snapshots of guava built from the master branch are available through maven using version head jre snapshot or head android snapshot for the android flavor snapshot api docs guava snapshot api diffs guava learn about guava our users guide guava explained a nice collection of other helpful links links github project issue tracker report a defect or feature request stackoverflow ask how to and why didnt it work questions guava discuss for open ended questions and discussion important warnings apis marked with the beta annotation at the class or method level are subject to change they can be modified in any way or even removed at any time if your code is a library itself i e it is used on the classpath of users outside your own control you should not use beta apis unless you repackage them if your code is a library we strongly recommend using the guava beta checker to ensure that you do not use any beta apis apis without beta will remain binary compatible for the indefinite future previously we sometimes removed such apis after a deprecation period the last release to remove non beta apis was guava 21 0 even deprecated apis will remain again unless they are beta we have no plans to start removing things again but officially were leaving our options open in case of surprises like say a serious security problem serialized forms of all objects are subject to change unless noted otherwise do not persist these and assume they can be read by a future version of the library our classes are not designed to protect against a malicious caller you should not use them for communication between trusted and untrusted code for the mainline flavor we unit test the libraries using only openjdk 1 8 on linux some features especially in com google common io may not work correctly in other environments for the android flavor our unit tests run on api level 15 ice cream sandwich references