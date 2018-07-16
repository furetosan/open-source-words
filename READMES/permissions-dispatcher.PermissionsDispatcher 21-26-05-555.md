permissionsdispatcher fully kotlin support special permissions support xiaomi support 100 reflection free permissionsdispatcher provides a simple annotation based api to handle runtime permissions this library lifts the burden that comes with writing a bunch of check statements whether a permission has been granted or not from you in order to keep your code clean and safe usage if youre using kotlin check kotlin ver first of all heres a minimum example in which you register a mainactivity which requires manifest permission camera 0 prepare androidmanifest add the following line to androidmanifest xml uses permission android name android permission camera 1 attach annotations permissionsdispatcher introduces only a few annotations keeping its general api concise note annotated methods must not be private annotation required description runtimepermissions ✓ register an activity or fragment we support both to handle permissions needspermission ✓ annotate a method which performs the action that requires one or more permissions onshowrationale annotate a method which explains why the permission s is are needed it passes in a permissionrequest object which can be used to continue or abort the current permission request upon user input onpermissiondenied annotate a method which is invoked if the user doesnt grant the permissions onneveraskagain annotate a method which is invoked if the user chose to have the device never ask again about a permission java runtimepermissions public class mainactivity extends appcompatactivity needspermission manifest permission camera void showcamera getsupportfragmentmanager begintransaction replace r id sample content fragment camerapreviewfragment newinstance addtobackstack camera commitallowingstateloss onshowrationale manifest permission camera void showrationaleforcamera final permissionrequest request new alertdialog builder this setmessage r string permission camera rationale setpositivebutton r string button allow dialog button request proceed setnegativebutton r string button deny dialog button request cancel show onpermissiondenied manifest permission camera void showdeniedforcamera toast maketext this r string permission camera denied toast length short show onneveraskagain manifest permission camera void showneveraskforcamera toast maketext this r string permission camera neverask toast length short show 2 delegate to generated class upon compilation permissionsdispatcher generates a class for mainactivitypermissionsdispatcher activity name permissionsdispatcher which you can use to safely access these permission protected methods the only step you have to do is delegating the work to this helper class java override protected void oncreate bundle savedinstancestate super oncreate savedinstancestate setcontentview r layout activity main findviewbyid r id button camera setonclicklistener v note delegate the permission handling to generated method mainactivitypermissionsdispatcher showcamerawithpermissioncheck this override public void onrequestpermissionsresult int requestcode nonnull string permissions nonnull int grantresults super onrequestpermissionsresult requestcode permissions grantresults note delegate the permission handling to generated method mainactivitypermissionsdispatcher onrequestpermissionsresult this requestcode grantresults check out the sample for more details other features getting special permissions maxsdkversion xiaomi since xiaomi manipulates something around runtime permission mechanism googles recommended way doesnt work well but dont worry permissionsdispatcher supports it check related pr for more detail intellij plugin androidannotations plugin if you use androidannotations you need to add androidannotationspermissionsdispatcherplugin known issues if youre in trouble check known issues list before filing an issue users thankfully weve got hundreds of users around the world download to add permissionsdispatcher to your project include the following in your app module build gradle file latest version is groovy dependencies implementation com github hotchemi permissionsdispatcher latest version annotationprocessor com github hotchemi permissionsdispatcher processor latest version snapshots of the development version are available in jfrogs snapshots repository add the repo below to download snapshot releases groovy repositories jcenter maven url http oss jfrog org artifactory oss snapshot local misc if you include jitpack io dependencies in your project it is important to review the order of the repositories available to your app module because of the librarys artifact id jitpack might be tempted to resolve the dependency on its own which could lead to an error during gradles configuration time if youre going to bump up the major version number we recommend to refer to migration guide licence copyright 2016 shintaro katafuchi marcel schnelle yoshinori isogai licensed under the apache license version 2 0 the license you may not use this file except in compliance with the license you may obtain a copy of the license at http www apache org licenses license 2 0 unless required by applicable law or agreed to in writing software distributed under the license is distributed on an as is basis without warranties or conditions of any kind either express or implied see the license for the specific language governing permissions and limitations under the license