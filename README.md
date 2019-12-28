# Phil's Lights

# Controller

The controller is made from two parts:
  - [WeMos D1 Mini](https://wiki.wemos.cc/products:d1:d1_mini) (natively 3.3vdc or 5vdc USB)
  - [WeMos DC Power Shield](https://wiki.wemos.cc/products:d1_mini_shields:dc_power_shield) (converts 7-24vdc to 5vdc)

The firmware that's loaded on the controller is called [WLED](https://github.com/Aircoookie/WLED) v0.9.0-b1.

When the unit is first powered, it will start in "AP Mode". Use a WiFi device to connect to the access point WLED-AP using the default password "wled1234". Go to the IP 4.3.2.1 in your browser (it may pop up automatically for you). You should also be able to use the embedded DNS server and connect to wled.me if in access point mode.

You can then set it up to connect to your WiFi Access point, once the settings are saved you may need to press the "reset" button on the side.

To easily discover and control the controller on the network, [download the WLED app](https://apps.apple.com/us/app/wled/id1475695033)

You can checkout the [WLED Wiki here for more info](https://github.com/Aircoookie/WLED/wiki)

Once open, check out the LED Settings page. I've already told it you have 450 leds (which should be 3 of those 150 LED strips) you can modify this though, if you have less or more than specified it won't hurt anything, just the animations may not work properly.

# Light strip info
When connecting light strips together, ensure that the data input (yellow/green from controller) enters the strip behind where the arrow is pointing. Thing of the data pin as a hose and it has to push in the direction of the arrow. As you add strips, you need to make sure that the arrows are oriented properly. Data MUST be connected in series, not parallel. Power (red/black) may be connected in parallel. Data (yellow/green) are the same signal line and can be combined into a single wire.

See diagram for a suggested wiring method. Power injected from one side and data daisy chained from end to starts. Note that the direction for the middle bank of LEDs are reversed so that the data injection is on the proper side.

IF you don't want to control the 3 strips independantly, you can actually run them all in the same direction, inject the data at the start of each strip, it will be treated as 150 LEDs vs 450. Whatever you do on strip 1, Led 1 will happen on Strip2/3 Led1 and so on... I wouldn't recommend this though, as it limits your flexibility (zoning off different areas, etc...)

![image](https://github.com/billchurch/phil_lights/raw/master/diagram.png)

# Connection diagrams

![image](https://github.com/billchurch/phil_lights/raw/master/IMG_0802.jpg)
![image](https://github.com/billchurch/phil_lights/raw/master/IMG_0803.jpg)
![image](https://github.com/billchurch/phil_lights/raw/master/IMG_0804.jpg)
![image](https://github.com/billchurch/phil_lights/raw/master/IMG_0805.jpg)