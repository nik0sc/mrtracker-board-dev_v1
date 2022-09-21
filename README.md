# mrtracker-board (dev_v1)

![c206ka8me2c91](https://user-images.githubusercontent.com/24191562/191492567-ccba766d-8f57-4265-adf1-96aee634c553.jpg)

![aphj56jne2c91](https://user-images.githubusercontent.com/24191562/191492186-cedd556e-8cf2-4fc7-a1ea-f8245a89366f.gif)

## What is this?

This is KiCAD schematic and board layout for MRTracker. BOM and centroid (pick and place) files are in the `assembly` directory.

MRTracker is a physical map of the MRT that tracks the location of trains in near real-time. It is a PCB with an array of LEDs on them and an ESP32 that gets the real-time location of trains. An LED will be lit for every train currently on the network. Currently the North-South and East-West lines are supported.

In the background, there is a web service that polls SMRT’s train API and transforms the arrival times of all lines at all stations into a map of individual trains on the network. (So, the accuracy of train locations is determined by the accuracy of these arrival timings.) The MRTracker board retrieves the map from this service periodically.

If you’ve seen traintrackr.io then this is something like that, but adapted for Singapore.

[Here is Geoff Marshall explaining traintrackr](https://www.youtube.com/watch?v=676xnII2OZg)

## Can I make it?

Sure, but firmware is not included. I made the board you see at the start of this README with [JLCPCB](https://jlcpcb.com/), they're pretty great.

**As-is**: No warranty express or implied of fitness for purpose. 

## Can I fork it, remix it, add the other lines, etc...?

Generally there is no copyright enforceable for hardware designs (weirdly there is an exemption for the highly secretive and competitive world of photolithography mask designs). So feel free.

## Known issues

- USB port GND pin is not connected (grounds through shield)
