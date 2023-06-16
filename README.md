#What is this project?
This project is a documentation and guide on how to replicate my personal improved SlimeVR build


# First things first, What is SlimeVR?

SlimeVR is a set of open hardware sensors and open source software that facilitates full-body tracking (FBT) in virtual reality. The project is built around creating a system that is customisable, hackable and can be modified to suit the needs of the user.


# Description
Currently there is one build that i made which uses the SlimeVR Hyperion Case. ( https://www.thingiverse.com/thing:5186756 )
The goal of this project is to make an easy to use guide on how to follow my specific build instructions, and get you set up easy. As always, feel free to improve my design.
The current design and build is V1.1

![afbeelding](https://github.com/Samstorm10/SlimeVR/assets/113670873/420b5567-d475-48f8-ad1e-da95aca8872f)



# Highlights
- Modified 3D printed case. The case makes it possible to program the WemosD1 without opening the device
- Cheap, but using the most reliable and best performance parts
- Custom simplified PCB design. Its an (almost) zero wire build. The only two wires that your build will include, is the battery wires.


![afbeelding](https://github.com/Samstorm10/SlimeVR/assets/113670873/f74c365e-9014-43cc-b89d-2ca07ccf33d9)

# Planned future improvements
- Adding diodes for extra protection
- Adding a 1.25 JST 4P connector for additional AUX support

# List of parts

You need the following parts to exactly replicate my build (for 5 slime VR trackers):

- 5X My modified 3D printed Hyperion Case design Print at 0.20mm layer height (Case.stl
- 5X My modified 3D printed Hyperion lid design. Print at 0.20mm layer height (Lid.stl)
- 5X My PCB design (See Gerber_V1.1.zip). Upload the design and order it as 1mm thickness PCB (You can upload and order them on like https://jlcpcb.com )
- 5X 3.7V 1800m Lithium Polymer LiPo Rechargeable Battery 804040 https://www.aliexpress.us/item/1005004147809952.html?gatewayAdapt=4itemAdapt
- 5X SS-12F23 switches https://aliexpress.com/item/4001202080623.html?spm=a2g0o.order_list.order_list_main.40.21ef79d2yO6ZZr&gatewayAdapt=glo2nld
- 5X BMI160 IMU https://aliexpress.com/item/4000052683444.html?spm=a2g0o.order_list.order_list_main.47.21ef79d2yO6ZZr&gatewayAdapt=glo2nld
- 5X TP4056 USB C charger board https://www.aliexpress.com/item/32649780468.html
- 5X Wemos D1 Mini (type C) https://aliexpress.com/item/1005005121150737.html?spm=a2g0o.order_list.order_list_main.29.21ef79d2yO6ZZr&gatewayAdapt=glo2nld
- 5X 180K Ohm Resistors https://aliexpress.com/item/1005002994755806.html?spm=a2g0o.order_list.order_list_main.157.21ef79d2yO6ZZr&gatewayAdapt=glo2nld
- 5X 1.25mm JST 2P headers connectors + wires https://aliexpress.com/item/1005004837848171.html?spm=a2g0o.cart.0.0.7c0161d7oyOV1r&mp=1&gatewayAdapt=glo2nld


# What tools do i need?

What you need:
- A soldering iron + soldering tin
- Basic electronics knowledge
- Wirecutter
- Isolation tape

What i recommend to also use:
- Helping hands for soldering
- A multimeter to check for shorting problems if needed
- Double sided tape


# Instructions

1. Solder the IMU160, Wemos D1 Mini and TP4056 Charger Board on the alocated spots on the PCB with the pin headers that were included with the parts
2. Solder the 180K Ohm Resistor to the PCB
3. Solder the 1.25MM JST connector to the PCB
4. Solder the SS-12F23 switch to the PCB
5. Now everything is soldered to the board itself. Cut off the pin headers at the bottom of your PCB and cover the bottom with isolation tape to make sure there won't be any accidental shorts
![afbeelding](https://github.com/Samstorm10/SlimeVR/assets/113670873/79075219-ddcc-4fb4-8c6f-af8129d5269d)
6. Put the 804040 battery into your case. Make sure that the wires will end up on the top right corner, otherwise the wires can't reach the jst connector.
7. If for some reason the battery will not sit snug into the case, use some thin double sided tape to secure it
8. Now insert the main PCB into the case on top of the battery. It should all be snug. If it doesn't, use some double sided tape on the bottom of your PCB
9. Next up, solder the red and black wires of the battery to the JST connector wires. For the current design, you need to put red to black, and black to red on the JST connector cable. Make sure to double check the + and - on the PCB design when plugging it in before testing.
10. Put some isolation tape on those exposed wires. See the image below for refence. This is what your project should look like now:

![afbeelding](https://github.com/Samstorm10/SlimeVR/assets/113670873/b9e306b3-ff03-4491-8238-6194378b50e4)


11. Plug in the JST cable into the connector on the PCB and switch the switch to the left and see if the device will power on. If it does, everything is alright and you can close it with the lid that you printed as well.
12. Flash the firmware by following the instructions of the official SlimeVR https://docs.slimevr.dev/firmware/index.html

You now have a working SlimeVR tracker. Repeat this proces 5 times and you got yourself a core movement kit!
