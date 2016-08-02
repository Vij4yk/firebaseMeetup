# firebaseMeetup

##Firebase Web App Development

Firebase is a slick backend cloud solution hosted by Google.  
*  We will share important information about the Firebase ecosystem available to web app developers.  
*  We will go over some Firebase data design concepts.  
*  Demonstrate how to connect a Firebase instance to your web application.






1- talk up firebase devs  ================================================================

firebase syronized data between client and server automagicly

developing a sucessful modern web app is not easy

you need back end data
you have to scale
you have to login users
you have to find users
you want analyicits
you have to make money

firebase has this
reach users
keep them engaged
scale
and get paid
test lab
reporting
real time database - file storage - hosting
aquire with invites = ad words - and dynamic links
authnication componet
notifications  - cloud messages - app indexing
remote config 
ad mob
analytics built for firebase
measure campains
users 
how they use the app


working as a one man gang
you can build your app
monitor crashes
optimize
find vauleable users


grow your user base
mainatain app quality
store and retrieve data





firebase + android => FirebaseUI
Events in Firebase are how you control the realtime synchronization of data in your app. This Firecasts explores each type of event and how it can be used when making an app. Also, for those interested in Android apps, we'll look at library called FirebaseUI that simplifies app development.
Want your RecyclerView to update in realtime? Use FirebaseUI! FirebaseUI is the easiest way to bind realtime data to ListViews and RecyclerViews. This Firecasts covers everything you need to know to be a pro at displaying lists of data in realtime.

firebase + angular => AngularFire
Want realtime data in your Angular app? Getting started with Angular and Firebase is super easy. Firebase has an official AngularJS library named AngularFire that makes binding data to your Angular apps a breeze. This video teaches you everything you need to know to get up and running fast.
Async data flow got you down? Get it under control with the $loaded() promise and the router.

firebase + ios
Getting started with Firebase and iOS is as easy as creating a Podfile. 

c++
web

https://firebase.google.com/docs/samples/





compact team: yo do not need backend engineers
fast iteration
scalable


realtime database
authentication
hosting





2- eco system  ================================================================
3- data design  ================================================================
firebase data types (4)
json tree

key/value pair
key are maps to values - the values below the keys
keys that do not have values (delete) are removed from key chain

bool  [true/false]
double [23.3456]
long [8765443]
string [this is a string]
firebase database is a json tree
the tree always ends with a real value leaf
data snapshots includes a key and everything below it
when you get many keys it becomes a list




Firebase Data Design
https://www.youtube.com/watch?v=rtuou_a-DHI

Understanding Firebase Database concepts 
https://www.youtube.com/watch?v=xuebjw_gP4M




4-firebase examples  ================================================================

Real Time Scheduling with AngularJS and Firebase
http://codepen.io/sevilayha/pen/vEEmMX

Simple chat app using firebase
http://codepen.io/iremlopsum/pen/ZWEdZj

ReactJS / Firebase to-do list
http://codepen.io/_massimo/pen/EKVVow

Simple Firebase Comments
http://codepen.io/joshbivens/pen/jbNJJR

Real-time Fridge Magnets
http://codepen.io/osublake/pen/gPeeJN

Test angular firebase chat app
http://codepen.io/baffleinc/pen/QNOZgp



Getting Started with Firebase on the Web - Firecasts 
https://www.youtube.com/watch?v=k1D0_wFlXgo&index=5&list=PLl-K7zZEsYLnJVX_0zbKytptZGugPIbJR

Introduction to Firebase Security Rules - Firecasts #7 
https://www.youtube.com/watch?v=eUfSpktxNeQ


Hit Counters & Timers in Vue + Firebase
http://codepen.io/mjweaver01/pen/reoKzp

AngularJs Firebase CRUD
http://codepen.io/aboudard/pen/XdogjG


AngularFire - Firebase/Angular Demo
http://codepen.io/joe-watkins/pen/KwEwYZ


Fire Table - Firebase & Angular
http://codepen.io/david-east/pen/ACalK



5-links  ================================================================

Check out the Firebase on web docs at https://goo.gl/RGrpOA
Read about it in our blog: http://firebase.googleblog.com

Add the Firecasts playlist! https://goo.gl/n2XqG1
Subscribe to the brand new Firebase Channel: https://goo.gl/9giPHG


Find out more at firebase.google.com/

Add the Introducing Firebase playlist! https://goo.gl/n2XqG1

Subscribe to the brand new Firebase Channel: https://goo.gl/9giPHG
Subscribe to Android Developers: goo.gl/ydHEAe
Subscribe to Chrome Developers: https://goo.gl/n7mBHx
Subscribe to Google Developers: http://goo.gl/mQyv5L




























-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-

-=-=--=-=-=-=-=-=
pricing
urls options
difference with db types
pros and cons
redis / couch / mongo

eco system
azure/aws competion up and comming
data design
code samples 
my code sample

-=-=-=-=-=-=-=-=-=-=-

-=-=-=-=-=-=-=-=-=-=-=-=-=-




=-=-=-=-=-=-=-=-=-=-=-=-=-=-=
Google Breakdown

Develop

Realtime Database
Authentication
Clould Messaging
Storage
Hosting
Remote Config
Test Lab
Crash Reporing



GROW

Notifications
App Indexing
Dynamic Links
Invites
AdWords



EARN

AdMob




-=-=-=-=-=-=-=-=-=-=-=-=-=-


use these stand alone or in concert

-=-=-=-=-=-=-=-=-=-=-=-=

	
You haven't really given us much info about what this data is going to be used for. I mean, you have said what data is going to be stored, but what are you going to do with it?

If your purpose is storing the data then reporting on it, then I think you're looking in the wrong place. A simple MySQL or SQL Database would do just fine and the reporting tools are readily available.

However if your going to be linking to something such as a web or mobile application where the data is constantly changing by multiple users (all accessing the same database stored in the cloud) then Firebase is the way to go.

So, your Pro's and Con's:

Pro's

If your app does run of a centralized DB, and is updated by a lot of users - then it's more than capable of handling the Real-Time data updates between devices.
Stored in the cloud so readily available everywhere.
Cross Platform API (If you are using this DB with an App)
They Host the data. -Meaning if you are storing a lot of data, you don't have to worry about hardware!

Con's:

Unless your app runs of one centralized database updated by a vast quantity of users, it's a major overkill.
Storage format is entirely different to that of SQL, (Firebase uses JSON) so you wouldn't be able to migrate that easily.
Reporting tools won't be anywhere near the ones of standard SQL.
Costs! -Limited to 50 Connections and 100mb of Storage!
You don't host the data, Firebase does. And depending on which server you get put on, viewing there up time there seems to be a lot of disruption lately.



-=-=-=-=-=-=-=-=-=-=-
register/ login with
email 
google
facebook
twitter
github

email address verification
passwrod reset

-=-=-=-=-=-=-=-=-=

realtime database

cloud hosted nosql database
synchronization conflict resolution
access directly from your app

-=-=-=-=-=
storage

easy file storage
handles poor connectivity
backed up and accessible from google cloud storeage


-=-=-=-=-=
hosting

server static assests
SSL by default


Install the Firebase CLI
Initalize your app
Add a file
Deploy your website



-=-=-=-=-=-==-=
Firebase is a NoSQL, real-time cloud database that super charges your web app development. With only a few lines of code, you are interacting with a hosted database that has user management built in and works with all major frameworks.

Join us for our inaugural meeting where we will go over the basics of Firebase -- how to create a Firebase and quickly store and retrieve data into your application. We'll be meeting at Galvanize - Golden Triangle and pizza and beer will be provided!



Firebase Web App Development

Firebase is a slick backend cloud solution.  We will share important information about the Firebase ecosystem available to web app developers.  We will go over some Firebase data design concepts.  How to connect a Firebase instance to your web application.



Firebase is a real-time, NoSQL cloud database that keeps development speed in mind. It not only gives you a database that can be accessed from the server, client, or mobile device, 
it also takes care of user authentication and hosting -- a complete backend solution! Plus, it's just been bought by Google, so long-term support and feature improvement is assured. 


Firebase is a NoSQL, real-time cloud database that super charges your web app development. With only a few lines of code, you are interacting with a hosted database that has user management built in 

we will go over the basics of Firebase -- how to create a Firebase and quickly store and retrieve data into your application.