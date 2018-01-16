# Dooruino
With this aruino project, you can use any cheap $5 arduino-like device to remotely open magnetic door lock.

![Dooruino](https://imgur.com/PV8F1cF.png)

## Requirements or components (Bill Of Materials)
* Arduino or arduino-like device ($10)
* Cables (just a few, $1)
* Audio speaker (if you want it to play music when door is opening - $2)
* Arduino Ethernet Shield ($7)
* SD Card is optional
* Ethernet cable ($2)
* Power source for arduino, 5v 1a ($2)
* *Total: $24*

## Idea
You're coming to office. Approaching the office door, you just press on the device screen icon which open specific page with password. You might enter the PIN password or save it right in your bookmarks. The door momentarly opens.

## Functions
* Get into the room or office by remotly entering PIN
* Access logs (optional)
* Access via internal network, IRC, Telegram or internet

![D2](https://imgur.com/ahshxYm.png)

## Project
The arduino has two devices: the ethernet shield (to get the command from the net) and speaker (to play a tone when door is opening or closing). Second device is optional. Arduino itself hosts a web page. It works with simple GET requests, when someone forms a specific request or enters the PIN on keyboard (that's on web page) the door opens. Keyboard has flexible design to open correctly on different devices.

## Features
* Remote interface, that works from any OS and device (Mobile Phone: Android, Firefox OS, Sailfish, iOS; Desktop laptop etc.)
* You can remotely unlock the door even being long distance away, even via IRC or Telegram etc. (might need a small bot-redirector)
* Self-watchdog which resets the device after some time

## How to use this repo in 10 steps
0) Install git, if you don't already (ubuntu: `sudo apt install git`)
1) Clone this repo: https://github.com/sxiii/dooruino
2) Download, install and start arduino IDE
3) Open downloaded dooru.ino file (dooruino folder) in the IDE
4) Press "upload" button & wait for upload to finish
5) Connect arduino to door lock (arduino PIN #2 and GND to door lock contacts)
6) Install Ethernet shield on the arduino & connect it to your local network
7) Optional step: connect speaker to contacts 8 and GND
8) Open web page of arduino IP address (default: 192.168.1.200) and try to enter PIN (default: 3214)
9) Profit!

## NOTES
* The default PIN is: 3214 (please give a second after pressing each button).
* The default IP is: 192.168.1.200
* The default MAC address of ethernet shield is: 00:05:B5:00:05:B5
* Wireshark program is helpful to research the (ethernet) output of arduino
* You can add the PIN after the URL of the arduino like this: http://aruino-ip/3214
* You can change the PIN yourself: ` if (readString.indexOf("3214 ") > 0  )`

## Future plans
* Make the device be compatible with different locks
* Security features (have to think about it more)
* Getting feedback & support

## Study time (let's say you know arduino)
* Learn how to work with arduino ethernet shield: 1 day
* Writing own sketch for the task: 1 day
* Total project time: 2 days

## Project presentation
https://docs.google.com/presentation/d/1YjkmqbQb2FImgZNrO74sPTNA0jRXeOzomwJ-jpKuo0Y

## Searching for developers and commits!
If you like this project and find it useful, please, improve it by your commits. Thank you!

## Contacts
Project creator & ideator: @sxiii (telegram: https://t.me/fakesnowden)
