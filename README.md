# Not-So-Basic-Arduino

### Table of Contents
* [HelloFunctions](#HelloFunctions)
* [LEDBlinkRevisited](#LEDBlinkRevisited)
* [FiniteLEDBlinker](#FiniteLEDBlinker)
* [NewPing](#NewPing)

## HelloFunctions

### Description
This assignment served as an introduction both to functions and the online Arduino editor that we're using for this year. The idea was to create a sketch with functions that would make a servo spin based on the distance from something that an ultrasonic sensor detected. Using functions to get the distance found by the sensor and to determine the speed of the servo, the code in the void loop section is greatly reduced; in fact, mine is six lines long. Most of the coding is concentrated in the make up of the functions.

### Wiring Diagram
<img src="images/wiring_hello_functions.png" alt="wiring diagram for HelloFunctions" height="300">

### Code
[Link to sketch](https://create.arduino.cc/editor/lgray52/ab9d6be7-250d-41d2-9c5f-ef9b109d3b19/preview)

### Reflection
This assignment was fairly challenging - my arduino skills were definitely rusty, and of course, I had to look several things up, like how to set up the ultrasonic sensor. The use of functions was a little bit confusing at first, but after re-reading the assignment a couple of times, looking up a couple things, and forming my first getDistance() function, it definitely got easier. I can see how they could be extremely useful in consolodating and cleaning up code. I didn't realise the servo was continuous at first, so I had to adjust my code, but other than that, there weren't too many surprises or difficulties that I can think of with the coding. The wiring was fairly straightforward - I connected the trigger pin of my ultrasonic sensor to digital pin 9 and my echo pin to 10, and my servo to pin 7, and the rest of the wiring from there was just attachments to ground and 5V.


## LEDBlinkRevisited

### Description
The idea of this assignment was to make a led blink, just a little bit more complicated. Using PWM pins and the "analogWrite" command, the point was to make an led fade in and out. Pretty simple, but a little bit tricky to figure out. For extra spice, an ectra challenge was to make a wave that reflected the brightness of the led in the serial monitor with dashes.

### Wiring Diagram
<img src="images/blink_wiring.png" alt="wiring diagram for led blink revisited" height="300">

### Code
[Link](https://create.arduino.cc/editor/lgray52/ae4aeb24-d5ce-494d-bbc1-d7caed13f2ca/preview)

### Reflection
This was an interesting assignment. After looking up (and figuring out) the "analogWrite" function, this project was pretty much all downhill, until it came to the wave in the Serial monitor challenge. I tried different combinations of using "analogRead" and trying to do it based on the brightness, but I couldn't get it to work. Mr. Dierolf helped out with this in class - this is where the "for" loop comes in. A "for" loop runs something repeatedly, based on it's instructions, which were determined by math in the case of this project. It seems honestly very useful. 

## FiniteLEDBlinker

### Description
The goal of this assignment is to use "if" statements to make an LED blink a finite number of times - I chose 5.

### Wiring Diagram
<img src="images/blink_wiring.png" alt="wiring diagram for finite led blinker" height="300">
(same as LED Blink Revisited)

### Code
[Link](https://create.arduino.cc/editor/lgray52/a6d3387a-8f2a-4b57-b37a-55ecb6fbe67d/preview)

### Reflection
This assignment was quite easy, having used Arduino last year. The idea is simply to blink a light 5 times and have it turn off. Pretty self-explanatory, just using an if statement and printing the counter to the serial monitor pretty much got the job done.

## NewPing

### Description
This used the NewPing library to control an ultrasonic sensor. By including the NewPing library, NewPing.h, in the code, it is easier to use an ultrasonic sensor, since the code of the library provides for it.

### Wiring Diagram
<img src="images/newping_wiring.png" alt="wiring diagram for NewPing" height="300">

### Code
[Link to code](https://create.arduino.cc/editor/lgray52/02b2e54c-c4b4-401f-a0b3-dcaa2544bffb/preview)

### Reflection
This assignment was good. I'm not sure if it's because we're doing this online, but some parts of the NewPing library commands simply wouldn't work, so i incorporated some of the code which I used in HelloFunctions to fill in the gaps. Other than that, there weren't any major difficulties I ran into. This is definitely a simpler way to use the ultrasonic sensors, so that should be useful.
