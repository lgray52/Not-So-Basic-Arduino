# Not-So-Basic-Arduino

### Table of Contents
* [HelloFunctions](#HelloFunctions)

## HelloFunctions

### Description
This assignment served as an introduction both to functions and the online Arduino editor that we're using for this year. The idea was to create a sketch with functions that would make a servo spin based on the distance from something that an ultrasonic sensor detected. Using functions to get the distance found by the sensor and to determine the speed of the servo, the code in the void loop section is greatly reduced; in fact, mine is six lines long. Most of the coding is concentrated in the make up of the functions.

### Image
<img src="images/wiring_hello_functions.png" alt="wiring diagram" height="300">

### Code
/*
  The goal of this sketch is to use functions to make a servo spin based on the distance from
  something that an ultra sonic sensors senses.
*/

int trigPin(9);
int echoPin(10);
float duration, distance; // this section sets up the ultrasonic sensor

int servoPin(7);
#include <Servo.h>;
Servo myServo; // this is how you include servo and above is servo library

void setup() {
  Serial.begin(9600);
  pinMode(trigPin, OUTPUT); // serves to set up ultrasonic sensor
  pinMode(echoPin, INPUT);

  myServo.attach(servoPin);
  myServo.write(85); // this project uses continuous servo, and for some reason, the stopping point was 85
}

int getDistance() { // the point of this code is to get an numerical value for the distance produced by the sensor
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW); // this sends out pulses from the sensor

  duration = pulseIn(echoPin, HIGH);
  distance = (duration * .0343) / 2; // time (duration)* speed(speed of sound, .0343 cm/microsecond) = distance (cm), divided by two because it has to go and come back

  Serial.print("Distance: ");
  Serial.println(distance);
  delay(1000);

  return distance; // returns distance to function
}

void servoFast() { // makes servo turn faster
  myServo.write(100);
  Serial.println("Fast");
}

void servoSlow() { // makes servo turn, but slower than servoFast()
  myServo.write(90);
  Serial.println("Slow");
}

void servoStop() { // 85 is the stopping point of this servo
  myServo.write(85);
  Serial.println("No");
}

void loop() {
  if (getDistance() < 10) // for a distance of less than 10 cm, "fast" is activated
    servoFast();
  else if (getDistance() < 30) // for a distance of less than 30 cm, "slow" is activated
    servoSlow();
  else // if these constraints aren't met, the servo doesn't move
    servoStop(); 
}



### Reflection
This assignment was fairly challenging - my arduino skills were definitely rusty, and of course, I had to look several things up, like how to set up the ultrasonic sensor. The use of functions was a little bit confusing at first, but after re-reading the assignment a couple of times, looking up a couple things, and forming my first getDistance() function, it definitely got easier. I can see how they could be extremely useful in consolodating and cleaning up code. I didn't realise the servo was continuous at first, so I had to adjust my code, but other than that, there weren't too many surprises or difficulties that I can think of with the coding. The wiring was fairly straightforward - I connected the trigger pin of my ultrasonic sensor to digital pin 9 and my echo pin to 10, and my servo to pin 7, and the rest of the wiring from there was just attachments to ground and 5V.
