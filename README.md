# firebaseMeetup 

##Firebase Web App Development

Firebase is a slick back end cloud solution hosted by Google.  
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
*  authentication component
*  google indexing
*  analytics built for firebase
*  ad mob

Work as your own compact team: Yo do not need back end engineers

=-=-=-=-=-=-=-=-=-=-=-=-=-=-==-=-=-=-=-=-=-=-=-=-=-=-=-=-=

# Firebase Ecosystem
##  Move over azure and aws
### We are doing it One Man Gang

![alt text](http://tech.co/wp-content/uploads/2013/02/Firebase.png)

### Using Firebase ecosystem help ease the pain, big business struggles with 
### synchronized data between client and server automagically

### Develop

*  Real time Database
*  Authentication
*  Cloud Messaging
*  Storage
*  Hosting
*  Remote Config
*  Test Lab
*  Crash Reporting

### GROW

*  Notifications
*  App Indexing
*  Dynamic Links
*  Invites
*  AdWords

### EARN

*  AdMob

[Firebase Documents](https://firebase.google.com/docs/)

[Firebase Libraries](https://firebase.google.com/docs/libraries/)

=-=-=-=-=-=-=-=-=-=-=-=-=-=-==-=-=-=-=-=-=-=-=-=-=-=-=-=-=

# Firebase Data Design
## JSON Tree

    Key / Value Pairs
    Keys are maps to Values 
     Values belong to Keys
     Keys that do not have Values are removed from Key Chain (deleted)

## Firebase Data Types 

Firebase offers four data types

*  boolean  [ True / False ]
*  double [ 23.3456 ]
*  long [ 8765443 ]
*  string [ This is a string ]

![alt text](http://i.stack.imgur.com/ooZyS.png)

     Firebase database is a JSON Tree
     Trees natural end points are leafs (Values)
     Data snapshots start with a (Key) and contain everything below it
     When you get many Keys it becomes a list

I know your thinking "Wheres The Beef"  

![alt text](http://26t4l93f9dhe439yxm286lpv.wpengine.netdna-cdn.com/wp-content/uploads/2015/07/maxresdefault-702x336.jpg)

Surprise! That is all we ever needed

[Firebase Data Design](https://www.youtube.com/watch?v=rtuou_a-DHI)
[Understanding Firebase Database concepts](https://www.youtube.com/watch?v=xuebjw_gP4M)

=-=-=-=-=-=-=-=-=-=-=-=-=-=-==-=-=-=-=-=-=-=-=-=-=-=-=-=-=

## Firebase Pro's

*  Real-Time data updates between lots of user devices to a centralized DB 
*  Stored in the cloud so readily available everywhere
*  Cross Platform API (If you are using this DB with an App)
*  Google Host the data so you don't have to worry about hardware
*  SSL by default

## Firebase Con's

*  Intended for only one centralized database per App 
*  Storage format is entirely different to that of SQL which can harder to migrate from JSON
*  Reporting tools won't be anywhere near the ones of standard SQL.
*  Costs soar up quickly - Limited Connections and Storage
*  Google Host your data, you do not

[Google Hosting](https://firebase.google.com/pricing/)

=-=-=-=-=-=-=-=-=-=-=-=-=-=-==-=-=-=-=-=-=-=-=-=-=-=-=-=-=

# Firebase Demos

Basically Firebase 
http://codepen.io/silicon_hacker/pen/bZxwVY

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

Hit Counters & Timers in Vue + Firebase
http://codepen.io/mjweaver01/pen/reoKzp

AngularJs Firebase CRUD
http://codepen.io/aboudard/pen/XdogjG

AngularFire - Firebase/Angular Demo
http://codepen.io/joe-watkins/pen/KwEwYZ

Fire Table - Firebase & Angular
http://codepen.io/david-east/pen/ACalK

This is a [Firebase Samples](https://firebase.google.com/docs/samples/)

=-=-=-=-=-=-=-=-=-=-=-=-=-=-==-=-=-=-=-=-=-=-=-=-=-=-=-=-=

# Firebase Links 

Find out more: 
firebase.google.com/

Firebase Blog: 
http://firebase.googleblog.com

Getting Started with Firebase on the Web: 
https://www.youtube.com/watch?v=k1D0_wFlXgo&index=5&list=PLl-K7zZEsYLnJVX_0zbKytptZGugPIbJR

Introduction to Firebase Security Rules:
https://www.youtube.com/watch?v=eUfSpktxNeQ

Firecasts playlist: 
https://goo.gl/n2XqG1

=-=-=-=-=-=-=-=-=-=-=-=-=-=-==-=-=-=-=-=-=-=-=-=-=-=-=-=-=

# Firebase Code Sample

```
<!doctype html>

<head>
    <script src='https://cdn.firebase.com/js/client/2.2.1/firebase.js'></script>
    <script src='https://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js'></script>
</head>

<body>
    <h2>Schedule Inputer</h2>
    <div id='scheduleList' style="background-color: aliceblue;"></div>
    <h3>Add To Schedule Inputer</h3>
    <table>
      <tr><td>Full Name:</td><td><input type='text' id='nameInput' placeholder='Name'></td></tr>
      <tr><td>Best Time To Call:</td><td><input type='text' id='callTimeInput' placeholder='Call Time'></td></tr>
      <tr><td>Message:</td><td><input type='text' id='messageInput' placeholder='Message'></td></tr>
    </table>

</body>

<script>
  // connection string to firebase
  var myDataRef = new Firebase('https://shining-inferno-5116.firebaseio.com/web/contact-us-data');
  
  // get user input values
  $('#messageInput').keypress(function (e) {
    if (e.keyCode == 13) {
      var name = $('#nameInput').val();
      var text = $('#messageInput').val();
      var calltime = $('#callTimeInput').val();
      
      // send values to firebase
      myDataRef.push({name: name, calltime: calltime, text: text});
      $('#nameInput').val('');
      $('#callTimeInput').val('');
      $('#messageInput').val('');          
    }
  });
  
  // add snapshot data from firebase
  myDataRef.on('child_added', function(snapshot) {
    var message = snapshot.val();
    displayScheduleList(message.name, message.calltime, message.text);
  });
  
  // paint snapshot data from firebase
  function displayScheduleList(name, calltime, text) {
    $('<div/>').text(text).prepend($('<i/>').text(calltime+' - ')).prepend($('<b/>').text(name+': ')).appendTo($('#scheduleList'));
    $('#scheduleList')[0].scrollTop = $('#scheduleList')[0].scrollHeight;
  };
  
</script>

</html>
```