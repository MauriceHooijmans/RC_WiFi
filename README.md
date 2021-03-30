# RC_WIFI
 Using NodeMCU to control RC servos and ESC thru WiFi.

#Credits
RC_WIFI.INO is based on code from https://github.com/programmer131/nodemcuCar/blob/master/carCode/carCode.ino

/data/virtualjoystick.js > is a modified version of https://github.com/jeromeetienne/virtualjoystick.js/blob/master/README.md

#upload to your NodeMCU
Note: before you upload the code make sure you have "ESP8266 Sketch Data Upload" installed
1.Upload the code from the .ino into your NodeMCU with the Arduino
2.Upload the data folder contents to SPIFFS https://github.com/esp8266/arduino-esp8266fs-plugin


#How to get ESP8266 Sketch Data Upload to upload to SPIFFS

1.Make sure you use one of the supported versions of Arduino IDE and have ESP8266 core installed.

2.Download the tool archive from releases page. > https://github.com/esp8266/arduino-esp8266fs-plugin/releases and download ESP8266FS-<most recent version>.zip

3.In your Arduino sketchbook directory, create "tools" directory (if it doesn't exist yet). > You can find the location of your sketchbook directory in the Arduino IDE at File > Preferences > Sketchbook location.

4.Unpack the zip file into "tools" directory (the path will look like <sketchbook directory>/tools/ESP8266FS/tool/esp8266fs.jar).
Note: On OS X and Linux based OSs create the tools directory in ~/Documents/Arduino/ and unpack the files there.

5.Restart Arduino IDE. < Important step else it will not be loaded and not show up in the menu.

sources :
https://github.com/esp8266/arduino-esp8266fs-plugin
https://www.instructables.com/Using-ESP8266-SPIFFS/

#Uploading to NodeMCU
1. Create a new sketch with the code from RC_WIFI.INO and save.
2. Go to sketch directory (choose Sketch > Show Sketch Folder).
3. Create a directory named "data" and copy the files from the data folder.
Note: Make sure you have selected a board, port, and closed Serial Monitor.
4. Select Tools > ESP8266 Sketch Data Upload menu item. This should start uploading the files into ESP8266 flash file system. When done, IDE status bar will display SPIFFS Image Uploaded message. Might take a few minutes for large file system sizes.