# Parse API Module PFObject Reference

_Please rate both the iOS and Android module in the marketplace if you find them useful :)_

[Click here to see version and release notes](./releasenotes.html)

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

____
____

##Table Of Contents

[TOC]

____
____

# PFObject Reference

____
____
## Types:

String - Javascript String Type

Boolean - Javascript Boolean Type Ex: `true false`

Number - Javascript Number Type

Date - Javascript Date Object Ex: `new Date()`

Map - Javascript object type with key-value pairs Ex: `{ name: "John", age: 45 }`

Array - Javascript array Ex: `new Array()`

Null - Javascript 	`null`

PFObject - Parse API PFObject Type

PFUser - Parse API PFObject Type

PFQuery - Parse API PFQuery Type

PFFile - Parse API PFFile Type

PFGeoPoint - Parse API PFGeoPoint Type

PFACL - Parse API PFACL Type

PFTypes - Parse API PFObject, PFUser, PFFile, PFACL, PFGeoPoint object

JSONTypes - String, Boolean, Number, Date, Map(of JSONTypes), Array(of JSONTypes), Null

Callback - a function with one argument Ex: `function(event) {  }`

TiBlob - Titanium Blob Type.

____
____
##Functions

###initWithClassName( className )

__Arguments:__

className: String

__Returns:__
	
void

----

###objectForKey( key )

__Arguments:__

key: String


__Returns:__
	
data: JSONTypes or PFTypes

_____

###objectForKeyInBackground( Map ) 

__/\*DEPRECATED\*/__

____

###setObject( data, key )

__Arguments:__

key: String

data: JSONTypes or PFTypes

__Returns:__
	
void

____

###removeObjectForKey( key )

__Arguments:__

key: String

__Returns:__
	
void

_____

###refresh()

__Arguments:__

void

__Returns:__
	
Map:	
	
	{
		succeeded: Boolean
		errorCode: Number
		error: String
	}

_____

###refreshInBackground( Map )

__Arguments:__

Map:
	
	{
		success: Callback
		error: Callback
	}

__Callbacks:__

success:
	event: Map
	
	{
		object: PFObject // The updated object
	}

error:
	event: Map
	
	{
		errorCode: Number
		error: String
	}

__Returns:__
	
void

_____

###save()

__Arguments:__

void

__Returns:__
	
Map:	
	
	{
		succeeded: Boolean
		errorCode: Number
		error: String
	}

_____

###saveInBackground( Map )

__Arguments:__

Map:
	
	{
		success: Callback
		error: Callback
	}

__Callbacks:__

success:
	event: Null

error:
	event: Map
	
	{
		errorCode: Number
		error: String
	}

__Returns:__
	
void

_____

###deleteObject()

__Arguments:__

void

__Returns:__
	
Map:
	
	{
		succeeded: Boolean
		errorCode: Number
		error: String
	}

_____

###deleteObjectInBackground( Map )

__Arguments:__

Map:
		
	{
		success: Callback
		error: Callback
	}

__Callbacks:__

success:
	event: Null

error:
	event: Map
	
	{
		errorCode: Number
		error: String
	}

__Returns:__
	
void

_____

###incrementKey( Map )

__Arguments:__

Map:
		
	{
		key: String
		byAmount: Number (OPTIONAL: The increment amount will default to 1)
	}

__Returns:__
	
void

_____

###fetch()

__Arguments:__

void

__Returns:__
	
Map:	
	
	{
		succeeded: Boolean
		errorCode: Number
		error: String
	}

_____

###fetchInBackground( Map )

__Arguments:__

Map:
	
	{
		success: Callback
		error: Callback
	}

__Callbacks:__

success:
	event: Map
	
	{
		object: PFObject // The fetched object
	}

error:
	event: Map
	
	{
		errorCode: Number
		error: String
	}

__Returns:__
	
void

_____

###fetchIfNeeded()

__Arguments:__

void

__Returns:__
	
Map:	
	
	{
		succeeded: Boolean
		errorCode: Number
		error: String
	}

_____

###fetchIfNeededInBackground( Map )

__Arguments:__

Map:
	
	{
		success: Callback
		error: Callback
	}

__Callbacks:__

success:
	event: Map
	
	{
		object: PFObject // The fetched object
	}

error:
	event: Map
	
	{
		errorCode: Number
		error: String
	}

__Returns:__
	
void

_____

###saveEventually()

__Arguments:__

void

__Returns:__
	
void

_____

###deleteEventually()

__Arguments:__

void

__Returns:__
	
void

_____

###isDataAvailable()

__Arguments:__

void

__Returns:__
	
Boolean

_____

###allKeys()

__Arguments:__

void

__Returns:__
	
Array of Strings


_____

____
____
##Properties


###acl

This is case sensitive. Make sure it's lowercase.

__Getter:__
	
PFACL

__Getter:__
	
PFACL

____

###className


__Getter:__
	
String

_____

###objectId


__Getter:__
	
Number

_____

###createdAt


__Getter:__
	
Date

_____

###updatedAt


__Getter:__
	
Date

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