# polymer-location

## This element is still in beta.  It has not yet been thoroughly tested, breaking changes are possible.

An element that allows you to declaratively access the GeoLocation api.

## How to install

    bower install polymer-location --save

## Documentation

### Example:

    <polymer-location></polymer-location>
    
## API Reference

### SHOW PRIVATE API
#### Properties
    
##### coords
User's coordinates property.
ex: <polymer-location coords="{{coords}}"></polymer-location>
Object
default: {"latitude": 0, "longitude": 0, "accuracy": 0, "altitude": null, "altitudeAccuracy": null, "heading": null, "speed": null}
readOnly
notify
reflectToAttribute

#### getLocation
Get's the users location once.  If you only need to get the location at page load there's no reason to send a 
value.  Otherwise you will need to bind it to a property with false as the value, and 
change the value to true when necessary.
ex: <polymer-location get-location></polymer-location>
Boolean
default: true

#### highAccuracy
This sets whether or not high accuracy is required when getting the user's location.
This is only used in conjunction with watch-location.
ex: <polymer-location high-accuracy="true" watch-location></polymer-location>
Boolean
default: false

#### maximumAge
Indicates how long to cache location results.  0 means don't cache, Infinity will
always pull from the cache.  This is only used in conjunction with watch-location.
ex: <polymer-location maximum-age="1000" watch-location></polymer-location>
Number
default: 0

#### timeout
Indicates how long to wait for a location response.  This is only used in conjunction
with watch-location.
ex: <polymer-location timeout="1000" watch-location></polymer-location>
Number
default: 5000

#### unsetWatch
Removes the watcher if watch-location has been called.  This is automatically called
on detached, so only use this if you have a reason to unset the watcher beforehand.
ex: <polymer-location unset-watch="{{unset}}" watch-location></polymer-location>
Boolean
default: false

#### watchLocation
When set this will watch the users location and update as the coordinate properties
change.  If you only need to watch the location from page load there's no reason to send a 
value.  Otherwise you will need to bind it to a property with false as the value, and 
change the value to true when necessary.
ex: <polymer-location watch-location></polymer-location>
Boolean
default: true
