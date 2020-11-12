# Not-So-Basic-Arduino

### Table of Contents
* [HelloFunctions](#HelloFunctions)

## HelloFunctions

### Description
This assignment served as an introduction both to functions and the online Arduino editor that we're using for this year. The idea was to create a sketch with functions that would make a servo spin based on the distance from something that an ultrasonic sensor detected. Using functions to get the distance found by the sensor and to determine the speed of the servo, the code in the void loop section is greatly reduced; in fact, mine is six lines long. Most of the coding is concentrated in the make up of the functions.

### Image
<img src="images/wiring_hello_functions.png" alt="wiring diagram" height="300">

### Code
<iframe src=https://create.arduino.cc/editor/lgray52/ab9d6be7-250d-41d2-9c5f-ef9b109d3b19/preview?embed style="height:510px;width:100%;margin:10px 0" frameborder=0></iframe>

### Reflection
This assignment was fairly challenging - my arduino skills were definitely rusty, and of course, I had to look several things up, like how to set up the ultrasonic sensor. The use of functions was a little bit confusing at first, but after re-reading the assignment a couple of times, looking up a couple things, and forming my first getDistance() function, it definitely got easier. I can see how they could be extremely useful in consolodating and cleaning up code. I didn't realise the servo was continuous at first, so I had to adjust my code, but other than that, there weren't too many surprises or difficulties that I can think of with the coding. The wiring was fairly straightforward - I connected the trigger pin of my ultrasonic sensor to digital pin 9 and my echo pin to 10, and my servo to pin 7, and the rest of the wiring from there was just attachments to ground and 5V.
