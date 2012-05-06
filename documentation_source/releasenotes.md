# Parse API Module Release Notes

_Please rate both the iOS and Android module in the marketplace if you find them useful :)_

[<- Go Back to Parse Module Guide](./index.html)

____
____
## Extra Reference

This guide contains examples and everything you need to know to start using the parse api module. 

The following reference files list all the functions, arguments, and return values for the Parse Module.

[Parse Module Guide](./index.html)

[Parse Module Reference](./parsemodulereference.html)

[PFObject Reference](./pfobjectreference.html)

[PFQuery Reference](./pfqueryreference.html)

[PFUser Reference](./pfuserreference.html)

[PFFile Reference](./pffilereference.html)

[PFGeoPoint Reference](./pfgeopointreference.html)

[PFACL Reference](./pfaclreference.html)

[PFFacebookUtils](./pffacebookutilsreference.html)

____
____

##Table Of Contents

[TOC]

____
____

##Versions

###Titanium iOS Module Version: 3.0
###Titanium Android Module Version: 3.0

____

###Current Parse iOS API Version: 1.0.2
###Current Parse Android API Version: 1.0.3

____

Please rate both the iOS and Android module in the marketplace if you find it useful :)  

Please if you want a new feature in Parse, Tell them! The more requests they get, the faster they implement certain features. Send them an email at [feedback@parse.com](feedback@parse.com)

I am in the process of making this documentation better and pushing new versions faster. So keep an eye out for that.

____

##Android Release Notes

###Version 3.0

- Parse is now out of beta
- Upgraded to module version 1.0

PFQuery

- __DEPRECATED__: `whereKeyContainedIn`. Use whereKey function instead.
- added the following arguments to `whereKey`: `containedIn`, `notContainedIn`, `withinGeoBoxFromSouthwest + toNortheast`, `matchesRegex + modifiers`, `matchesQuery`
- added: `addAscendingOrder`, `addDescendingOrder`, `getFirstObject`, `getFirstObjectInBackground`

PFObject

- added: `saveEventually`, `deleteEventually`, `fetch`, `fetchInBackground`, `fetchIfNeeded`, `fetchIfNeededInBackground`, `isDataAvailable`, `allKeys`
- __DEPRECATED__: `objectForKeyInBackground`
- __CHANGED__: Changed the `ACL` property to `acl` because it was causing case sensitive errors.

PFACL  

- added: `getPublicReadAccess`, `getPublicWriteAccess`, `getReadAccessForUserId`, `getWriteAccessForUserId`, `getReadAccessForUser`, `getWriteAccessForUser`

ParseModule  

- added: `PFObjectCreateObjectWithoutData`, `PFObjectFetchAll`, `PFObjectFetchAllIfNeeded`, `PFObjectFetchAllInBackground`, `PFObjectFetchIfNeededInBackground`

###Version 2.0.1

- Added support for Android Push Notifications
- Added Error Codes 123, 124, 125.
- Added support for GeoPoints and ACLs
- Other bug fixes.

###Version 1.0

- Everything is implemented except for the new ACL and push notifications.
- Supports PFObject, PFUser, PFFile, PFQuery
- Parse still has no support for Facebook on Android.
- Added Android Documentation

____

##iOS Release Notes

###Version 3.0

- Parse is now out of beta
- Upgraded to module version 1.0

PFQuery

- __DEPRECATED__: `whereKeyContainedIn`. Use whereKey function instead.
- added the following arguments to `whereKey`: `containedIn`, `notContainedIn`, `withinGeoBoxFromSouthwest + toNortheast`, `matchesRegex + modifiers`, `matchesQuery`
- added: `addAscendingOrder`, `addDescendingOrder`, `getFirstObject`, `getFirstObjectInBackground`

PFUser

- __DEPRECATED__: `facebookId`, `hasFacebook`, `linkToFacebookInBackground`, `unlinkFromFacebook`, `unlinkFromFacebookInBackground`

PFObject

- added: `saveEventually`, `deleteEventually`, `fetch`, `fetchInBackground`, `fetchIfNeeded`, `fetchIfNeededInBackground`, `isDataAvailable`, `allKeys`
- __DEPRECATED__: `objectForKeyInBackground`
- __CHANGED__: Changed the `ACL` property to `acl` because it was causing case sensitive errors.

PFACL  

- added: `getPublicReadAccess`, `getPublicWriteAccess`, `getReadAccessForUserId`, `getWriteAccessForUserId`, `getReadAccessForUser`, `getWriteAccessForUser`

ParseModule  

- added: `PFObjectCreateObjectWithoutData`, `PFObjectFetchAll`, `PFObjectFetchAllIfNeeded`, `PFObjectFetchAllInBackground`, `PFObjectFetchIfNeededInBackground`
- __DEPRECATED:__ `PFUserLoginWithFacebookInBackground`, `FacebookSessionIsValid`, `FacebookSessionExpirationDate`, `ParseHasFacebookApplicationId`, `FacebookRequestWithGraphPath`, `FacebookRequest`, `FacebookDialog`
- added property: `pfFacebookUtils`

PFFacebookUtils

- added singleton object to use Facebook Utilities. Can only be retrieved from ParseModule.pfFacebookUtils property
- added: `FacebookRequestWithGraphPath`, `FacebookRequest`, `FacebookDialog`, `loginInBackground`, `linkUserInBackground`, `unlinkUserInBackground`, `shouldExtendAccessTokenForUser`, `extendAccessTokenForUserInBackground`, `extendAccessTokenIfNeededForUserInBackground`, `isLinkedWithUser`


###Version 2.0.2

- Added Error Codes 123, 124, 125.
- Added support for GeoPoints and ACLs
- Other bug fixes.

###Version 1.3.3

- __IMPORTANT:__ Versions older than 1.3.3 for this module for iOS were packaging the entire Parse framework with your application. This bug has now been fixed. So you will have a smaller app size.

###Version 1.3.2

- __IMPORTANT:__ When using the User Sign Up or Login, the `username, email, password` arguments are now all __CASE-SENSITIVE__. This was done to prevent errors with locales.
- Fixed minor bugs and documentation errors
- Updated example app.js to prepare for Android Parse Module
- Fixed/Added Facebook Methods in ParseModuleReference Documentation
- Added className property to PFQuery
- Added Android Documentation
- Fixed documentation. Replaced PFQueryGet with PFQueryCreate.
- Added documentation on how to update objects and users.
- PFObjectSaveAllInBackground now has a callback

###Version 1.3.1

- Fixed minor issue: Emails are now optional when signing up a PFUser. 

###Version 1.3

- Fixed memory leaks.

- Added guidelines and helper functions for using Titanium Blobs with PFFile

- Added the following functions to Parse Module for PFFile
	- `PFFileCreateFileWithNameAndData`
	- `PFFileCreateFileWithData`
	- `setDefaultTiBlobImageRepresentation`
	- `getTiBlobDefaultImageRepresentation`
	- `willTiBlobBeSavedWithDefaultImageRepresentation`

- Added the following constants to Parse Module for PFFile 
	- `kTiBlobImageDefaultPNG`
	- `kTiBlobImageDefaultJPEG`

- Added PFFile Support

- Added Push Notification Support

- Added the following functions to Parse Module for Push Notifications  
	- `ParseiOSPushStoreDeviceToken`
	- `ParseiOSPushHandlePush`
	- `ParseiOSPushSubscribeToChannel`
	- `ParseiOSPushSubscribeToChannelInBackground`
	- `ParseiOSPushUnsubscribeFromChannel`
	- `ParseiOSPushUnsubscribeFromChannelInBackground`
	- `ParseiOSPushSendPushMessageToChannel`
	- `ParseiOSPushSendPushMessageToChannelInBackground`
	- `ParseiOSPushSendPushDataToChannel`
	- `ParseiOSPushSendPushDataToChannelInBackground`
	- `ParseiOSPushGetSubscribedChannels`
	- `ParseiOSPushGetSubscribedChannelsInBackground`	

- Fixed: Before you weren't able to store PFObjects, PFUsers, and PFFiles in other PFObjects. Now you can! So Associations Work!

- Fixed: Wasn't able to test on device due to XCode's new policy of "defaulting to armv7 architecture". Not a problem anymore! Both armv6 and armv7 supported.

- Added warning to documentation that you should only require the module once in your application's namespace.

- Added documentation on refreshing the Logged In User on application resume for Android and iPhone

- Added PFQuery Caching Support

- Added the following functions to PFQuery
	- `countObjects`
	- `countObjectsInBackground`
	- `whereKeyContainedIn`

- Added the following properties to PFQuery
	- `skip`

- Added more informative error descriptions

- Added the following properties to PFUser
	- `isAuthenticated`
	- `isNew`
	- `facebookId`
	- `hasFacebook`

- Added the following functions in Parse Module
	- `PFRequestPasswordResetForEmail`
	- `PFRequestPasswordResetForEmailInBackground`
	- `PFQueryCreateUserObjectWithId`
	- `PFQueryCreateQueryForUser`
	- `PFQueryCreateObjectOfClassAndId`
	- `PFQueryCreateQueryWithClassName`
	- `PFObjectCreateObjectWithClassName`
	- `PFObjectSaveAll`
	- `PFObjectSaveAllInBackground`

- Added the following properties in Parse Module
	- `ParseHasFacebookApplicationId`
	- `FacebookSessionIsValid`
	- `FacebookSessionExpirationDate`

- Implemented Facebook Functions from Parse In Parse Module:
	- `PFUserLoginWithFacebookInBackground`

- Implemented Facebook Functions from Parse In PFUser:
	- `linkToFacebookInBackground`
	- `unlinkFromFacebook`
	- `unlinkFromFacebookInBackground`
	- `setPassword`

- implemented Facebook Public API Functions in Parse Module:
	- `FacebookRequestWithGraphPath`
	- `FacebookRequest`
	- `FacebookDialog`

- Added more examples to the `app.js` file in `./examples/`


###Version 1.2

- Fixed: The Parse Framework was not being located correctly. You can now put the module in the default Titanium Module Directory or in your project's module directory.


###Version 1.1

- Bug: The Parse Framework was not being located correctly.

###Version 1.0

- Initial Release
- No support for caching or push notifications yet.
  
  
____
____
## Release Notes 

[Click here to see version and release notes](./releasenotes.html)

____
____
## Author

Programmer: David E. Rodriguez

Company: Forge42

Website: www.forge42.com

Twitter: @programmerdave

____
____
## Feedback and Support

If you find any bugs, please let me know.

Also when reporting a bug or problem, please send me your iOS `build.log` file in your e-mail if using the iOS version of the module.

Please direct questions, feedback, and concerns about this module to [support@forge42.com](support@forge42.com)

Please include __Parse API Module iOS Support__  
or __Parse API Module Android Support__ in the subject line.

I will get back to you in a timely manner.

Please if you want a new feature in Parse, Tell them! The more requests they get, the faster they implement certain features. Send them an email at [feedback@parse.com](feedback@parse.com)

____
____
## License

IMPORTANT: This module is unofficial and is not maintained by parse.com

Copyright(c) 2011 by Forge42. 

Please see the LICENSE file included in the distribution for further details.

[<- Go Back to Parse Module Guide](./index.html)
