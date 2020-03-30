# makecounter.js is small control to animate counter

author Alejandro Landini [landini.com.ar](http://landini.com.ar/)

version 1.0

copyright © 2020 Alejandro Landini

name l-makecounter
type  jQuery

## tutorial

 This control has two functions:


    $(element).mcounter(); //is the js constructor that allows to reform any element in an animated counter. option values can be passed to it.
    $('.counter').visibilityChanged (); 


    This second method activates the counters on the screen, if these are visible, the counter starts. option values can be passed to it.
    use HTML attr start counter without js


    <span class="counter" id="counter-lat" data-endcountvalue="3801"></span>


 param {Boolean} runOnLoad - true start counter is visible on load page
 param {Number} frequency - 100ms, time to check if the control chague vsibility
 param {Number} startcountvalue - start count value in counter
 param {Number} endcountvalue - end count value in counter
 param {Number} elapsetime -in seconds, elapse time to finish count

## Requires library

    <script> src="https://code.jquery.com/jquery-3.4.1.min.js"></script>
    <script> src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.2.6/gsap.min.js"></script>

## Example

Simple usage example:

    $('#sales').mcounter({
        endcountvalue: 4002,
        startcountvalue: 3995,
        elapsetime:8
    });
    $('.counter').visibilityChanged({
        callback: function(element, visible, initialLoad) {
            // do something
            console.log("visible?: " + visible);
        }
    });
