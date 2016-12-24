adt-pulse - A Javascript library for ADT Pulse
======================

This module provides a Javascript library for calls to the ADT Pulse AJAX backend.  Since it is dependent on a
production website, the behavior is subject to change without notice.

This is a derivative of the [node-adt-pulse](https://www.npmjs.com/package/node-adt-pulse) module.  The related git repository is not active and does 
not contain the source for that module, so this is not a true fork.

Installation
-------
You can install through npm: `npm install adt-pulse`

Usage
----

    var Pulse = require('adt-pulse');
    var myAlarm = new Pulse('<Your Email>', '<Your Password>');
    
    // Register Callbacks:
    myAlarm.onDeviceUpdate(
        function(device) {
            console.log(device)
        }
    );
    
    // Login - gets all devices, zones and status and invokes callbacks:
    myAlarm.login();