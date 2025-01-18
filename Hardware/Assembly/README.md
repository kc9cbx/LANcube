## Build and Assembly

Please carefully review the included pictures to get an idea of what the final product should look like.
![Full](./images/Full.JPG)
![Overveiw](./images/Overview.JPG)
![Top Layout](./images/Top_Layout.JPG)
![Inside Lid](./images/Inside_Lid.JPG)
![Top View](./images/Top_View.JPG)
![Bottom View](./images/Bottom_View.JPG)
![Wired](./images/Wired.JPG)

#### Before you start
 - Use the gerber files in the Hardware folder and order control and main PC board from the board house of your choice (JLCPCB, PCB GOGO, PCB WAY, etc.) 
 - Obtain all the parts listed in the Parts section
 - 3D print the enclosure for the control board
 
![Main PCB Front](./images/LAN3_Main_Board_v1.4_Front.png)
![Main PCB Back](./images/LAN3_Main_Board_v1.4_Back.png)
![Wired](./images/LAN3_Interface_Board_v1.4_Front.png)
![Wired](./images/LAN3_Interface_Board_v1.4_Back.png)


#### Start with assembling the control panel/control board.
 - Drill and cut necessary holes/openings 
   - Place the blank control PCB on the bottom of the 3D printed enclosure and mark off where to drill for PCB standoffs; drill the necessary holes.
   - About 1/2 way down the long side of the control board enclosure, cut in a slot to feed through  the flat ribbon cable - about 3mm width and length that is about double the width of the FCC cable. The side where you cut in the slot will be the top of the control board enclosure.
   - On this same side of the enclosure, drill two holes for screws that will be used to mount the control panel enclosure to the main box
 - Solder all the components
   - Place and solder the 4 pushbuttons onto the PCB
   - Solder on the header pins onto to the display
   - Solder the display onto the front PCB
   - Insert the FCC connector from the back of the board and solder it in place
 - Assemble the control panel
   - Mount the PCB onto standoffs
   - Feed through the screws that will be used to mount the control panel assembly to the main box, and secure them in place with nuts
   - Connect ribbon cable to the FCC connector on the back of the control board
   - Feed the cable trough the slot on the box
   - Slide the PCB on standoffs and secure it to the bottom of the box
![Complete Control Panel](./images/Complete_Control_Panel.JPG)
![Control Panel Top](./images/Control_Panel_Top.JPG)
![Control Panel Bottom](./images/Control_Panel_Bottom.JPG)

#### Assemble the main board
 - Prepare all components
   - Solder header pins onto the GPS module
   - Solder header pins onto the fuel gauge - 1 set of 2 pins, and tw2 sets of 3 pins
   - Solder header pins onto the charging board - you will need 4 individual pins
   - Solder header pins onto the Pololu electronic switch - one set of 6 pins and one set of 7 pins
 - Solder everything onto the main board
   - Start with raspberry pi pin headers. To determine correct length, first, mount 20mm standoffs onto the bottom of the main board. Push the headers onto the raspberry pi and then place the main PCB over the headers. At this point, take a moment to verify that there is a 3-4mm clearance between the main board and the metal of the USB and ethernet port on the Pi - we want to make sure that nothing will short out once components are soldered onto the main board.
   - With everything in place like this, solder the headers to the main board. Once soldered, trim off the excess from the top.
   
![Pin Placement](./images/Pin_Placement.JPG)
![Board Placement](./images/Board_Placement.JPG)

   - Remove the main board from the pi
   - Solder the FCC connector
   - Solder the 5 7-pin connectors
   - Solder the GPS module
   - Solder the electronic switch
   - Solder the two capacitors - pay attention to polarity
   - Solder the fuel board
   - Solder the charging board
   
![Complete Board](./images/Complete_Board.JPG)

#### Prepare the sensors
 - Sensor wiring is relatively simple - it is straight through, pin for pin. Pin 1, as marked on the main board, connects to VIN on the sensor, Pin 2 is wired to GND on the sensor, etc. Please take a look at the picture on what the finished sensor looks like. 
 - Also, please note the orientation of the soldered wires - they are turned inwards, towards the center of the sensor. While this is not crucial, this orientation makes it easier to hide the wires once sensors are mounted.
 - Lastly, you can use heat shrink to protect the solder points on the sensor module board, just be careful to not cover up or obstruct the sensor.

![Sensor Wiring](./images/Sensor_Wiring.JPG)

#### Prepare the main box
 - Before assembly, drill all the necessary holes
   - On the bottom/lid drill 4 holes for the Raspberry Pi, 4 holes for tripod mount (centered), 2 holes needed to mount the control panel, hole for the USB C bulkhead connector, and lastly, the slot for the ribbon cable
   - On the main part of the box drill three hole for each sensor - one that is large enough to feed through the harness connector and two needed to mount the sensor. When determining the mounting location, mark the hole placement so that sensor is placed in the center of that side of the box. 
   - Optional - if used, drill the necessary holes to mount the bubble level
   
![Top Drill](./images/Top_Drill.JPG)
![Bottom Drill](./images/Bottom_Drill.JPG)
![Sensor Holes](./images/Sensor_Holes.JPG)

#### Determine which side/sensor will be the front and MARK IT.
 - When choosing the front, it is very convenient to choose the side that is either to the left or the right of the side where control panel will be mounted. As LAN3 is most often used on the top of the vehicle, choosing one of these sides will make it easy to access controls from either driver or the passenger side of the vehicle, without having to remove it from the roof.
 - Draw arrows that point towards the front, on both the inside and the outside of the LAN3

#### Mount all the sensors
 - Mount the prepared sensors to the box using short standoffs or alternatively, nuts as spacers.
 - Mark the end of each cable harness with the side on which sensor is mounted - top, front, back, left, and right
 - Once sensor is mounted, cover the opening for the harness and mounting screws with black Gorilla tape. This will prevent light from the inside of the box from reaching the sensor.
   
#### Mounting the Battery and GPS antenna
 - This is a tricky one, as both are mounted to the top of the main box. We will use the two brass insets at the top of the box to do this. You will need piece of plastic that is slightly smaller than the inner dimension of the box. You can use ABS, acrylic, or really any type of plastic of the right size. Drill 2 holes into the plastic so that they align with brass insets. It is recommended that you obtain countersunk screws for this.
 - For the GPS antenna, you will sandwich it between the box and the plastic sheet, then screw the plastic sheet to the box. As battery will go over the top of the screws, place a piece of thick/heavy tape over the screws to protect the battery - black Gorilla tape works great for this. 
 - Before the battery is installed, it needs to be protected from physical damage. Use 70mm heat shrink to do this, but be VERY CAREFUL when applying heat shrink to not overheat the battery.
 - Once battery is protected, use double sided tape + gorilla tape to secure the battery to the top of the box

#### Mount components to the lid 
 - Install the tripod mount
 - Install the USB C bulkhead connector
 - Feed through the ribbon cable and mount the control panel box
 - Finally, mount the Raspberry Pi, using standoffs that are tall enough to keep it away from the protruding screws 
 
#### Connect the GPS
  - Use the extension cable to connect the GPS antenna to the U. FL/I-PEX connector on the GPS board

#### Connect the USB C
 - Connect the USB C connector on the charging board to the USB-C bulkhead connector using the right-angle USB-C cable
 
#### Connect the control panel
 - Connect the ribbon cable from the control panel to the FFC connector on the main board
 
#### Connect all the sensors
 - Connect each sensor to the corresponding connector on the main board - each connector is labeled on the main board. Incorrect sensor placement will give you incoherent results.

#### Finally, connect the battery - EXCERCISE EXTREME CAUTION WITH BATTERY POLARITY
 - Please note that JST battery connectors are NOT STANDARD, not all are wired in the same, and may be wired EXACTLY BACKWARDS from what you need. Before connecting the battery, please verify that positive/red wire is closest to the capacitors. Main board under the fuel gauge also has "+" marking on the correct side. If your battery/connector are backwards, you can use a thin blade to carefully lift up the clip holding each wire in the connector and swap their positions to get correct polarity.
 - Once you've verified the polarity, connect the battery
 - As the final hardware check, connect a charger to the USB-C connector on the outside of the case, and you should see charging board battery level LEDs turn on

With the hardware complete, go to the software section to learn how to prepare the SD card.

![Testing](./images/Testing.JPG)