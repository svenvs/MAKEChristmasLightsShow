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

So, if you have all the things from the shopping list you can start by prepping your PC. first lest verify if you need to install a driver or not. go too this link: inprogress...
Then connect the NODEMCU with your computer. and do what is asked on the screen. If it says great success you are good. Else install the driver: https://sparks.gogo.co.nz/ch340.html. if that does not work please try a different usb cable

All connections working? Great lets move on!

## WLED installation

Of course we are super lazy so we want to do as little as possible. and for instead of programming a whole app there where some cool people that already did. And we are going to use that! :D

Go too this website: https://vstr.dev/MAKE/ and connect your node mcu to the computer. follow the instructions on the page. When the upload is complete great job, you have now programmed a NODE MCU without even touching code! :D

You can disconnect the NODEMCU from your computer

Is the website not able to flash your nodeMCU no problem go to this link: https://github.com/svenvs/MAKEChristmasLightsShow/blob/main/troubleshooting/oldfasionedFlash.md and here a new guide that can help you flash your nodeMCU

## Let's hookup some wires

Please make sure you first flash the NODEMCU before connecting the LED's. It’s for the stability of flashing the NODEMCU. the LED's might draw too much power...
Disconnect the NODEMCU from your PC.

NODE MCU      | LED STRIP
------------- | -------------
VIN           | Red wire
G             | Black wire
D4            | Yellow or white wire start with yellow

When you have the wires correctly plugged in and you power the NODEMCU with your phone charger. the LED's will turn orange

## Configure WLED

If you go to your mobile phone and have a look for wifi networks you will find a new wife network called: WLED-AP you can login to that network with the default password: **wled1234**

And you will see the welcome screen:
![WLED welcome screen](/assets/wledwelcome.PNG)

Now click on WIFI SETTINGS and update the wifi settings too the one in your house.

![WLED welcome screen](/assets/wledwifisettings.png)

When done it might be ok to reboot the device by just pulling the plug and connecting it again.
Also put your phone back to use your wifi.

### discover WLED

When you open the app and it will tell you there you need to add your wled click on the + sign in the right top corner. and it will give you this screen:

![WLED welcome screen](/assets/wleddiscoverlights.jpeg)

If you click on discoverlights it will start scanning your wifi network to find your wled. After a wile it will say found WLED and then you can hit the check mark to get back to the home screen. where it will show you your wled:

![WLED welcome screen](/assets/wledapphomescreen.jpeg)

If the app did not find your LEDS it might be that the wifi settings of the previous step did not workout properly. Check if you see a WLED-AP wifi network again. if that is not there you need to reflash the device and start over. You could try setting up the network connections with your computer. This might help only you will lose internet connection of your PC for a bit.

If the LEDs are found :D
Click on your Wled and have fun! start playing around also check effects :D. When you are done playing get back to the tutorial :D

---

Get back to the slides

## Xlights first start

First it will ask where you want to save all the files.

![WLED welcome screen](/assets/xlightsfirststartshowdir.PNG) give it a nice location what you like best

when that is done we have to set up the connection between xlights and WLED. on the left you can find the button Add ethernet click on that one and it will open a settings page on the right. these are the value's you need to set it with: *Only the important ones are given the rest leave as default or empty

Atribute                 | Value
------------------------ | -------------
Name                     | A cool name you like BlazingChristmasBASHLights
Autosize                 | Unchecked (FALSE)
Vendor                   | WLED
Model                    | WLED
Variant                  | Generic ESP8266
IP adress                | IP adress can be found in wled app
Start universe           | 1
Universe count           | 1
Channels per universe    | 90

here a print screen of my config:
![WLED welcome screen](/assets/xlightswledsettings.PNG)

Now lets see if the connection works or not. On the top left corner you see a tab tools go there and click on test. You will see a screen like this:

![WLED welcome screen](/assets/xlightsTestConnection.PNG)

Now fiddle around with the buttons and if all done correctly you will see your lights blinking etc.

## Xlights lightshow layout

Before we can start making our lightshow we have to make our layout. This is basically taking a picture of all our LED's we have setup around our house ;) ;). for now you can just make a picture of your LED strip and email it to yourself.

to upload your picture, click on the layout tab in xlights. and then on the left side you can find background image. there you can add it. Its nice to play with the darkness to darken the picture abit so that you can see the colors later.

![Xlight layout tab](/assets/xlightsLayout.png)

### Adding a model

Now to show Xlights where our LED strip is in the picture we are going to create a so called model. to do this on the right side you see some buttons we are going to create a single line click on the button as seen in the image and draw a single line. Keep your mouse button down and release when you are happy with the line.

![Xlight layout tab](/assets/xlightsSingleline.png)

Now on the left side we need to assign which lights our line represents. These are te settings you need too change:

Atribute                 | Value
------------------------ | -------------
Name                     | A cool name you like BlazingChristmasBASHLights
Nodes/String             | 30
Controller               | Use start channel (for mac users the controller can aslo be used but start channel is more stable)
Start channel            | 1

These are mine settings:

![Xlight layout tab](/assets/xlightslinesettings.png)

Done? Perfect now let’s test out your model. by going again to the testing pane (tools -> test) and click on the models tab. start playing around with the radio buttons again. if your LED strip is responding you are good to continue.

## Xlights Sequencing a light show

🎵 And its now the wonderful time of the MAKE sessioooon 🎵 We are now going to add our cool music sequence to make our LED's DANCE!!!

First we need to go to the Sequencer tab. when you landed there you can click this button: ![Xlight layout tab](/assets/XlightsNewSequence.png) and it will ask you and then click the big red button musical sequence. Select your fantastic christmas song and click on 20fps. And on quick start.

Now you are all ready to start creating nice sequences.

On the top left you can find some preinstalled effects. In mid right you can see your waveform of the music track. below there you can see the models. You now have only 1. you can drag and drop the effects inside the black area. then on the moment of time of the music that effect will appear on the lights. Lets start simple by just dragging the BARS in there. see the image:

![Xlight layout tab](/assets/seq.png)

In the settings panel you can change the direction of the bars. from up to down or left to right etc etc.

When you have your sequence ready and want to enjoy your show. you can click on the light bulb button ![Xlight layout tab](/assets/lightbulb.png) on the far right. to output to the lights. and click on the Play button ![Xlight layout tab](/assets/play.png)  to start your show.

Enjoy!