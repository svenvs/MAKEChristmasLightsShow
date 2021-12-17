# Maunal flash of the NODEMCU

First download the following files:

* esp home flasher
* binary of WLED

When both are downloaded execute the esp home flasher by right click and run as administrator.

It will present you with a screen like this:
![WLED welcome screen](/assets/esphomeflasher.jpeg)

Now connect your NODEMCU with your USB cable if you have not done so. And click on the refresh icon. then open the drop down and select the COM port the number can be different.

![WLED welcome screen](/assets/esphomeflasherCOM.jpeg)
If there are more shown and you dont know which one you should choose. just disconnect the NODEMCU hit the refresh button. and see which number is gone. Now you know which one you have to choose :D.
If none are popping up. then please make sure you installed the drivers. And verify your USB calbe it might be only charging instead of also transferring data.

When you have selected your NODEMCU select the .bin file as firmware it looks like something like this. When selected hit Flash ESP and it will start uploading the application to your NODEMCU

![WLED welcome screen](/assets/esphomeflasherBIN.jpeg)
