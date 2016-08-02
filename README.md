# firebaseMeetup

##Firebase Web App Development

Firebase is a slick backend cloud solution hosted by Google.  
*  We will share important information about the Firebase ecosystem available to web app developers.  
*  We will go over some Firebase data design concepts.  
*  Demonstrate how to connect a Firebase instance to your web application.






=-=-=-=-=-=-=-=-=-=-=-=-=-=-==-=-=-=-=-=-=-=-=-=-=-=-=-=-=

# The One Man Gang

![alt text](https://s-media-cache-ak0.pinimg.com/564x/d1/eb/b0/d1ebb0b1daa52ed832faeed9ff0c939e.jpg)

-= ERR ... A One Man Firebase Gang 

## You are the One Man Gang

*  you need back end data
*  you have to scale
*  you have to login users
*  you have to find users
*  you want to know what users are clicking
*  you have to make money

## Working as the One Man Gang

*  real time database and file storage 
*  cloud hosting scalability
*  authnication componet
*  google indexing
*  analytics built for firebase
*  ad mob

Work as your own compact team: Yo do not need backend engineers

=-=-=-=-=-=-=-=-=-=-=-=-=-=-==-=-=-=-=-=-=-=-=-=-=-=-=-=-=
# Firebase Ecosystem
##  Move over azure and aws

![alt text](http://tech.co/wp-content/uploads/2013/02/Firebase.png)

## Developing a sucessful modern web app is not easy
### Using Firebase ecosystem help ease the pain, big business struggles with 
### syronized data between client and server automagicly

### Develop

*  Realtime Database
*  Authentication
*  Clould Messaging
*  Storage
*  Hosting
*  Remote Config
*  Test Lab
*  Crash Reporing

### GROW

*  Notifications
*  App Indexing
*  Dynamic Links
*  Invites
*  AdWords

### EARN

*  AdMob


This is a [Firebase Samples](https://firebase.google.com/docs/samples/)


=-=-=-=-=-=-=-=-=-=-=-=-=-=-==-=-=-=-=-=-=-=-=-=-=-=-=-=-=

# Firebase Data Design
## JSON Tree

    <blockquote>
        <p>Key / Value Pairs</p>
        <p>Keys are maps to Values </p>
        <p>Values belong to Keys</p>
        <p>Keys that do not have Values are removed from Key Chain (deleted)</p>
    </blockquote>

## Firebase Data Types 
Firebase offers four data types
*  bool  [true/false]
*  double [23.3456]
*  long [8765443]
*  string [this is a string]

Surprise! That is all we ever needed

![alt text](http://i.stack.imgur.com/ooZyS.png)


    <blockquote>
	<p>Firebase database is a JSON Tree</p>
	<p>Trees natural end points are leafs (Values)</p>
	<p>Data snapshots start with a (Key) and contain everything below it</p>
	<p>When you get many Keys it becomes a list</p>
    </blockquote>


[Firebase Data Design](https://www.youtube.com/watch?v=rtuou_a-DHI)
[Understanding Firebase Database concepts](https://www.youtube.com/watch?v=xuebjw_gP4M)

=-=-=-=-=-=-=-=-=-=-=-=-=-=-==-=-=-=-=-=-=-=-=-=-=-=-=-=-=

# Firebase Demos

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


