jquery.double-keypress
=========================

A jQuery plugin to manage double keypress.

Requirements
====

* [jQuery](https://jquery.com/)

Installation
=====
Using bower is the simplest way.

    bower install jquery.double-keypress --save-dev

Usage
====

**Simple Way**

    $(function(){

		var keyCode = 16;   // means SHIFT key (and means any if null)

		$('body').dbKeypress(keyCode, function(e){

			alert('SHIFT key was double-pressed');

		});

    });
    
**with Options**

    $(function(){

        var keyCode = 16;
        var options = {

            eventType: 'keydown',   // Optional (keydown or keyup)
            interval: 350,          // Optional (milliseconds)
            callback: function(e){

                alert('SHIFT key was double-pressed');

            }

        };
        $('body').dbKeypress(keyCode, options);

    });
    
**Multiple keyCodes**
    
    $('body').dbKeypress([16, 17], function(e){

        if(e.keyCode == 16) {

            alert('SHIFT key was double-pressed');

        } else if(e.keyCode == 17) {

            alert('CTRL key was double-pressed');

        }

    });
    
**About KeyCode**

See [here](http://www.cambiaresearch.com/articles/15/javascript-char-codes-key-codes)

Contributor
==

[sdavidg](https://github.com/sdavidg)


License
====

This package is licensed under the MIT License.

Copyright 2015 Sukohi Kuhoh