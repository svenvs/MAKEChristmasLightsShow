# MAKEChristmasLightsShow

Hi and welcome to the MAKE session where we are going to create a crazy light show!

Before we start I want to make sure you have the folowing things with you:

* Your wifi ssid
* Your wifi pass
* The NODE MCU/ wemos (ESP 8266)
* Jumper cables
* LED strips
* USB power adapter minimum 500 mili amps (most phone chargers will do)
* Micro USB cable that is able too transfer data

So if you have all the things from the shopping list you can start by prepping your PC. first lest verify if you need to install a driver or not. go too this link: inprogress...
Then connect the NODEMCU with your computer. and do what is asked on the screen. If it says great success you are good. Else install the driver : https://github.com/nodemcu/nodemcu-devkit/tree/master/Drivers. if that does not work please try a different usb cable 

All connections working? Great lets move on!

## Lets hookup some wires!

IMG wirering

NODE MCU      | LED STRIP
------------- | -------------
VIN           | Red wire
GND           | Black wire
D4            | Yellow or white wire start with yellow

So all wired up? still no lights ? yeah that is correct :D we must first install some software on the NODE MCU to make it doo something

## WLED installation

Go too this website: https://vstr.dev/MAKE/ and connect your node mcu to the computer. follow the instructions on the page. When the upload is complete great job you have now programmed a NODE MCU without even touching code ! :D 

You can disconnect the NODEMCU from your computer 

## Configure WLED

ok now disconnect the NODE MCU from your computer and hook it up to your phone charger. We wont need to connect it anymore to the computer. :D 
If you go too your mobile phone and have a look for wifi networks you will find a new wife network called: WLED-AP you can login to that network with the default password: **wled1234**

And you will see the welcome screen: 
![WLED welcome screen](/assets/wledwelcome.PNG)

Now click on WIFI SETTINGS and update the wifi settings too the one in your house.

![WLED welcome screen](/assets/wledwifisettings.png)

When done it might be ok to reboot the device by just pulling the plug and connecting it again. 
Also put your phone back to use your wifi. 

### discover WLED

When you open the app and it will tell you there you need too add your wled click on the + sign in the right top corner. and it will give you this screen:

![WLED welcome screen](/assets/wleddiscoverlights.jpeg)

If you click on discoverlights it will start scanning your wifi network too find your wled. After a wile it will say found WLED and then you can hit the check mark to get back to the home screen. where it will show you your wled:

![WLED welcome screen](/assets/wledapphomescreen.jpeg)

Click on your Wled and have fun! star playing around also check effects :D. When you are done playing get back tho the tutorial :D


## install Xlights

Now you have seen the nice effects its time to led your LEDS DANCE !!! :D this is what we are going to do with a software called Xlights. 

first go to the Xlights website and download the software: https://xlights.org/releases/

follow the installation instructions 

## Xlights first start
First it will ask where you want to save all the files.

![WLED welcome screen](/assets/xlightsfirststartshowdir.PNG) give it a nice location what you like best

when that is done we have too set up the connection between xlights and WLED. on the left you can find the button Add ethernet click on that one and it will open up a settings page on the right. these are the value's you need to set it with: *Only the important ones are given the rest leave as default or empty

Atribute      | Value
------------- | -------------
Name          | A cool name you like
Autosize      | Unchecked (FALSE)
Vendor        | WLED
Model         | WLED
Variant       | Generic ESP8266
IP adress     | IP adress can be found in wled app
Start universe      | 1
Universe count      | 1
Channels per universe      | 90

here a print screen of my config:
![WLED welcome screen](/assets/xlightswledsettings.PNG)

Now lets see if the connection works or not. On the top left corner you see a tab tools go there and click on test. You will see a screen like this:

![WLED welcome screen](/assets/xlightsTestConnection.PNG)

Now fiddle around with the buttons and if all done correctly you will see your lights blinking etc.
