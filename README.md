meteor-loginWithPassword-TypeError
==================================

Reproduction app for loginWithPassword TypeError in Meteor


How app was created
===================

* meteor create loginWithPasswordTypeError
* cd loginWithPasswordTypeError
* meteor add accounts-password
* meteor remove insecure
* meteor remove autopublish
* meteor


Steps to reproduce TypeError
============================

* git clone https://github.com/pwldp/meteor-loginWithPassword-TypeError
* cd meteor-loginWithPassword-TypeError
* meteor
* open Mozilla Firefox on site http://127.0.0.1:3000
* open WWW Console
* run in console code: `Meteor.loginWithPassword('admin','password',function(err,res){if (err) console.log("Error: "+err);});`

And see in console log:

Meteor.loginWithPassword('admin','password',function(err,res){if (err) console.log("Error: "+err);});
undefined
TypeError: mutating the [[Prototype]] of an object will cause your code to run very slowly; instead create the object with the correct initial [[Prototype]] value using Object.create meteor.js:451
"Error: Error: User not found [403]"
