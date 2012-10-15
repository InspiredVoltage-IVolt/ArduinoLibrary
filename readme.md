# ![ArduinoLibrary]

## c# library to send messages to arduino pins with actuators attached

This is a library of classes to hopefully make it easy to communicate with an arduino via usb.  It was originally developed for a much larger project involving an event library controlling arduino drummers (which i will put on GitHub soon).

The code includes a test console application to demonstrate how to set up and arduino connection, upload code and send pin messages.

This is my first GitHub experiment, any contributions or criticisms are more than welcome!  The code is reasonably well commented, but if you need better explanations, please ask.

## Demos

Some examples of this being used to power a robbot drummer are on this [youtube playlist](http://www.youtube.com/playlist?list=PLD92D7DB13BC6AF1A)

## Code Description

# ArduinoLibrary

Classes to help connect and send messages.  You must define a device, it's pin configurations and the actuators attached to the pins.  There is also some players which help to sent messages with turn a pin off after a certain amount of time.

Probably stepping through the test project is the best way to understand.

# ArduinoLibrary.SketchUploader

Classes used to compile and upload sketch style code to the arduino

This has a dependancy on having the arduino v1.01 software installed
http://arduino.googlecode.com/files/arduino-1.0.1-windows.zip

Important: There is a bug in the avrdude.exe that comes with the arduino software
so you need to replace it with the version posted on this page
http://code.google.com/p/arduino/issues/detail?id=806

Thanks to Sittipong Jansom http://arduinosketch.codeplex.com/ for some bits of code and inspiration

PLEASE NOTE: this has only been tested on an atmega2560 so far but it should work with any arduino device that is listed in the arduino boards.txt

# ArduinoUploadTest

I'm not really sure how to unit test something easily that is so dependant on physical outputs, so this file contains two tests.

The first test uploads some code to make the LED blink.  The second uploads some interactive code and then send a few pin events out to the device.  You might need to change the location of your arduino IDE installation and the com port that the device uses.

## License

BSD License  
http://www.gnu.org/licenses/gpl.html
Copyright (c) Keith Urquhart
