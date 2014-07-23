meteor-loginWithPassword-TypeError
==================================

Reproduction app for loginWithPassword TypeError in Meteor reported in [Issue 2327 ](https://github.com/meteor/meteor/issues/2327)


Create app
==========

* meteor create loginWithPasswordTypeError
* cd loginWithPasswordTypeError
* meteor add accounts-password
* meteor


Steps to reproduce TypeError
============================

* open Mozilla Firefox (I use FF ver. 30.0 on Linux Ubuntu 14.04) on URL: http://127.0.0.1:3000
* open WWW Console (Ctrk+Shift+K)
* run code in console: `Meteor.loginWithPassword('admin','password',function(err,res){if (err) console.log("Error: "+err);});`

And see in console log:

- Meteor.loginWithPassword('admin','password',function(err,res){if (err) console.log("Error: "+err);});
- undefined
- TypeError: mutating the [[Prototype]] of an object will cause your code to run very slowly; instead create the object with the correct initial [[Prototype]] value using Object.create meteor.js:451
- "Error: Error: User not found [403]"
