## Setting up software and provisioning the LAN3 

#### Preparing the Card
Download the zip file containing the LAN3 SD card image from the Releases. Unzip the image – resulting file will be around 3.5Gb 

Follow the process outlined here: https://raspberrytips.com/create-image-sd-card/ to expand LAN3 image on to the SD card. 
 
To validate that your SD card was created correctly. Insert it into the LAN3 device and power it on. Keep in mind that first boot after card is created will take a while as image will re-size itself to fit the card and then reboot. If your GONet hardware is working correctly and the SD card was imaged correctly, after a couple of minutes, the display will turn on and you will see, on the very first line, “PROVISION” followed by a version number. 
 
#### Provisioning
Press the power off button to turn off the device. Once all lights have turned off, remove the SD card and place it back in your computer.
 
Download and open the provided LAN3Config.conf file. In the file, update the text in the quotes on the first line. This will set the name for your LAN3. For example, to name the LAN3 MyLAN3001, the first line should look like this:
HostName="MyLAN3001"

At this time, only the first line is used, so you can disregard the rest of the file.
 
Once you have the LAN3Config.conf updated, copy it on your LAN3 SD card into /fsboot/.
 
Place the SD card into the LAN3 and turn it on. It may take several minutes for provisioning to complete, as multiple automatic reboots are required, so please be patient.
 
Once provisioning is complete, the display will come on and you will see your LAN3 name at the very first line, indicating that provisioning was successful.

#### Hotspot
After provisioning, LAN3 will create its own hotspot, with the same name as the LAN3. When this happens, using the examle from above, you will see “HOTSPOT: MyLAN3001” on the display. You can connect to that hotspot using the password “Remote4LAN3” (capitalization matters!)
