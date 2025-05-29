---
title: "Hydra"
author: "bcon"
description: "multi head 3d printer with automatic toolchanging"
created_at: "2025-05-15"
---

## **5/15/2025 Log 1: The Beginning**

I set up my repo, the onshape docs, and the other documents I am using to track my research. I also will make a pr on the hack club github once my project is approved. 

Spreadsheet Here: https://docs.google.com/spreadsheets/d/1dxXwSJXcaqQSJZOgLCcOFMtPYZC8gTVC_DopSeNoC-k/edit?gid=0#gid=0

I am planning to start off my doing some drawing and idea generation using paper and MS Paint, after which I will go into CAD and start laying everything out. 

Time Spent: 15 Minutes

5/15/2025 Log 2: Ideation

After talking with one of my robotic mentors, I determined a few crucial details that will help move my design forwards. I looked at the Bambu Lab X1C and found out that they only used 1 stepper motor to drive the z axis using a timing belt. This was huge as it means I can get away with a [BTT Octopus Pro 1.1 Board](https://biqu.equipment/products/bigtreetech-octopus-pro-v1-0-chip-f446?variant=40144816767074) with 8 stepper drivers. This allows me to use 1 motor on z, 1 on A, 1 on B, and then have 5 slots left over for 5 toolheads! I was originally worried about having enough slots as I had already thought about multiple motors for z, but this solves all of my issues! I have put the picture of the Bambu and a drawing below. 

![Bottom of the X1C](https://cdn-forum.bambulab.com/original/3X/4/e/4eaea6886d38b572c5476957a8a062e6ea47568e.webp)

![First Idea](https://github.com/user-attachments/assets/6c60a9bc-2513-4067-8761-e16e68037779)

This allows me to have up to FIVE toolheads on the printer! While also simplifying my z axis and making it super simple. Now it is time to go to some simple sketches in Onshape to begin the process.

Time Spent: 1 Hour

## **5/16/025 Log 2: This is going to be fun**

I started my CAD work to knock out some general sizes from which i will design the rest of the printer. 

![image(2)](https://github.com/user-attachments/assets/38d6a12f-e4a4-4263-a9f4-301e3c42bba8)

The idea here is that I have 5 bays for each toolhead, each of which I am aiming to have be less than 2.5in wide. In the picture above, I drew what I mean. My goal is to have the fan and duct for part cooling will stay on the toolhead to reduce complexity and part count. Then, the extruder/nozzle will swap in and out. I can forsee a potential problem later on with wiring, but that is a later me issue. The hardest part is going to be figureing out a secure way to actually change between the toolheads, as since I am not using a flying gantry, the latching system is going to be a little harder as there are very few examples for that to go off of. I have a few ideas to make it work, but I want to dive a little deeper into them before I flesh them out in CAD.

Other than that, I started my mastersketch for the frame, from which I will derive the 3D CAD from such that I can easily adjust dimensions if I need more speed. Here is the general idae for how space will be laid out. 

![general idea](https://github.com/user-attachments/assets/27e8b088-10b5-4473-be7e-dd22ed6a3e5c)

Time Spent: 1.5 Hours

## **5/16/2025 Log 3: Pogo Pins and Starting the CAD**

I first started by doing some frame work with the design. I have decided for my mental sanity that all of the 2020 extrusion will just be a 20mmx20mm rectangle, as trying to make the extrusion work for BISMUTH in Onshape was extremely annoying. 

![Screenshot 2025-05-16 172515](https://github.com/user-attachments/assets/8203852f-2f3f-4b88-ac7a-74155f4707da)

From here, I will do some more sketching to get my z axis locked in. 

Then, I did some research and ideas for my toolhead power and transfer. After some research and discussion with some people, I found something called a pogo pin connector. This allows a non locking system in which I can change my toolhead and provide power with the same wires. 

![toolchangfe 1](https://github.com/user-attachments/assets/635f1724-bb57-4b7d-9daa-52c17a98cb52)

After a LOT of research, I determined that this would be viable. I then decided to do some drawing of a possible hotend idea. 

![hotend_idea](https://github.com/user-attachments/assets/fcdde9bc-730a-4677-8ed2-7640d90f8737)

The idea is that the hotend and extruder swap, and get power through pogo pins. This allows for one set of wires powering everything. I have to figure out the custom PCB for my toolhead, along with doing lots of math to calculate exactly what I need. On top of that, I have to do some firmware stuff to ensure that losing communication with the thermistor wont through a bunch of errors once the printer is actually up and running. I plan to move forward with the CAD and get the z axis figured out first. Hopefully, this system should allow for a cheaper, easier, simpler way to have a multi head printer. 

Total Time Spent: 2 Hours

## **5/16/2025 Log 4: Frame**

I spent some more time today working on the starting frame CAD. I also did some drawings for the kinematic system. Below are screenshots of my current state. 
![kinematics](https://github.com/user-attachments/assets/71b89c42-71c5-40a9-a606-734f1996527d)

This shows the possible kinematic system!


![Screenshot 2025-05-16 201911](https://github.com/user-attachments/assets/2d9a6cf4-8a62-457d-94d6-9de530792046)

The original frame design

![Screenshot 2025-05-16 222258](https://github.com/user-attachments/assets/620368a4-19bf-4dcc-a942-8d430ea4aee2)

My newest frame design! This is the one I am going forward with. It uses a combo of metal plates and 3d prinmted brackets for stiffness. I have drawn out the 3D printed brackets that will additionally stiffen the frame up. 

I also determined that, if I go forward with my pogo pin idea, I actually have an additional four stepper motor slots than I additionally had to begin with! This means that I can either find a different board, or I have some extra slots to play around with. Maybe I can go for triple z on the axis, or maybe I can go for 2 motors on A and B for more speed, or... the possibilities are endless! 

Time Spent: 2 Hours

## **5/18/2025 Log 5: CoreXY

I made huge progress on my kinematic system today! Took almost the entire day but I got it done. 

![image](https://github.com/user-attachments/assets/f6254d2a-b544-4216-9a04-b1b16d7a76a2)
![image](https://github.com/user-attachments/assets/3afbfb91-132f-40b0-9b1b-000fcce6eb54)
![image](https://github.com/user-attachments/assets/ac0ad034-2516-4e68-9e7a-04b3789a7308)
This core-xy system uses 2 motors with 2 independent belts rigged as seen above to power the system. This is a typical motion system for 3D printers. Through the development of this system, I had to increase the frame size quite a bit unfortunately. However, after all is said and done this is looking good. I still have to add belt tensioners once I figure out my toolhead. 

I also did extreme research into the toolchanger. Based off of my options, it is looking like I am going to need an active toolchanger in order to make this work. I have been researching possible ways and hopefully will have something to show soon!

Time Spent: 6 Hours

## 5/22/2025 Log 6: ToolChanger V1

After taking a short break to finish up school and have some personal time, I am moving forwards with my design by ironing down a few key features: what my toolhead consists of. 

Extruder - [ProtoXtruder 2.0 ](https://github.com/nhchiu/3DPrinter-Designs/tree/main/ProtoXtruder_2.0) - I chose this extruder for the price and quality, along with being able to manufacture it myself.
Hotend - Some Bambu Lab Clone due to the price and various options available. This allows me to easily swap in higher quality versions for different filaments
Toolhead Board - EBB 36 v1.2 - This is a solid, cheap board with everything I am looking for. 
Special Stuff: I am going to try to make a toolhead "Hat" to put onto my board with pogo pins that will allow me to power my individual toolheads from the same board. This has both pros and cons, but I have decided to move forwards with this idea as it is unique and interesting. 

My goal is to have 5 or 6 toolheads, depending on how many I can fit in my printer. The more the better, and I can always easily add them on later. I may also have another idea that will allow me to double that, but we will leave that in the brain for now...

![wiring diagram](https://github.com/user-attachments/assets/bddee1d2-0f32-4443-9799-550dfa4d34c5)
Here is my wiring diagram for going from the motherboard to the toolhead.

I also put the cad together and started to form my toolhead, but it is still a very rough design right now.

I am also deciding on switching my motherboard, most likely, and going forwards with a 3 motor kinematic bed z design, unlike the original one motor z design that I first had. 

Time Spent: 3 Hours

## 5/22-23/2025 Log 7: Toolhead CAD

I started to put my ideas for the toolhead into cad. Here is the general idea behind my toolhead.

![image](https://github.com/user-attachments/assets/039f03df-eeb1-46a0-9f87-fe4ff5aef5dd)

Then, I put these ideas into real life. This took multiple hours of design work, thinking, and cross referencing from drawings and designs found on the web. 

![image](https://github.com/user-attachments/assets/66395b69-b9b6-4ff4-b08b-ad8300222716)

The first version looks like so. It uses a spring and a servo actuated latch to open and close. 

![image](https://github.com/user-attachments/assets/c844efc2-a617-42b1-9983-555dc4353b3d)

It uses two standard mk8 brass nozzles mounted to the part on the spring to self center in two holes on the toolhead, along with a pair of magnets to align. When the servo releases, the spring pushes up, locking the toolhead into place. 

![image](https://github.com/user-attachments/assets/ec0b1e8c-79d2-4828-a879-4c26ead7bc5b)

Then, there are 4 magnets and 2 rods that make up the dock for the toolhead. The toolhead will be mounted like so to the frame. This will be the next thing I do. 

![image](https://github.com/user-attachments/assets/47580b20-056a-41aa-8999-384e3083f51b)

Finally, I have to rethink how I power this, as there is very little room for my pogo pins. I may have to go with a standard umbilical rather than this new idea for space purposes, but we will see how much space I have once I finish everything else. 

Next Steps: I am going to work on a second version of the toolchanger, get some air ducts in there, and get the toolhead dock cadded and mounted. Basically, everything except the power and the z axis. 

Time Spent: 8 Hours over the two days.

## 5/24/2025 Log 8: ToolChanger V2

I was not happy with the first version of my toolchanger, so I made some changes. To start, I replaced the linkage with a direct drive servo. Per my math, the servo should have enough force to compress the spring 10mm. Additionally, I modified the geometry to be better optomized. 

![image](https://github.com/user-attachments/assets/73195d06-5974-449e-b7b5-aeaf6ae87c8e)

I also put in heat set inserts to mount the back part. I decided to split these parts in order for better printability.

![image](https://github.com/user-attachments/assets/ad1ff9df-dfc2-4dad-b379-750cf4f9df5a)

The final fan duct is also in the CAD now, thanks to Rolohaun and his crossxy printer. I am going to connect that to either a 5015 blower fan or a 4028 blower fan for part cooling. I will also mount the auto bed leveling, most likely a BL touch onto that part as well. I am unsure what I am going to do with the rest of the space. Tomorrow, I will work on my belt clamps, fan mount, and ABL mount to finish up the toolhead. 

Time Spent: 3 Hours

## 5/25/2025 Log 9: ToolHead Updates!

I have successfully finished the first (and second and third and fourth) version of my toolhead! 

![image](https://github.com/user-attachments/assets/1f6296e0-1f77-4e15-ba41-2f2b11927105)

Utilizing the BTT EBB 36 Toolhead Board, a Bambu Lab Clone Hotend, my custom toolchanging mech, and a 5015 blower fan for part cooling, this thing sits at just under 2.125 inches wide! This allows me to fit 6 toolheads in my designated dock space! I currently plan to make one of them a designated ABL dock with just something like a BL Touch, so there will be 5 distinct toolheads at this moment. Today, I not only added in the custom fan ducts, but added in spots for belt wrap, as well as shortened my overall width. Additionally, I modified my overall frame size in order to comfortably fit my 300mm x 300mm bed - which I have decided to use due to the fact that it is more common to find parts for cheap for that bed size. It also allows me to use all 400mm linear rails instead of a mix of 350mm and 400mm.

![image](https://github.com/user-attachments/assets/915ea041-8975-477e-8e82-dfddb020717d)

Current CAD. 

Up Next: Toolhead Dock, Z Axis, and Electronics Mounting

Time Spent: 5 Hours

## 5/26/2025 Log 10: Toolhead Dock!

![image](https://github.com/user-attachments/assets/0d24410b-e6bb-4af3-b1d3-55e651eb390d)

I spent this time creating the docks for my toolheads. They utilize 4 6mm OD x 2mm WD magnets along with 2 5mm Steel Rods to dock the toolhead. The magnets line up with the magnets on the toolhead.

![image](https://github.com/user-attachments/assets/816adb27-f1e9-4550-bec3-2768b979f93e)

All together, I can fit 6 docks, and this is the full assembly with them. They attach to the 2020 extrusion that runs across the printer. 

![image](https://github.com/user-attachments/assets/bb55819b-4848-4c3b-b892-76223806135a)

Finally, I decided to make one of the toolheads purely a bed leveling probe. This is because I don't see a need for more than 5 toolheads, along with decreasing complexity on the main toolhead. If needed, I can figure something else out later and add in the 6th toolhead. 

All in all, this was a smaller amount of time spent, but certainly a lot more fruitful. 

TIme Spent: 3 Hours

## 5/27/2025 Log 11: Starting Z!

After finishing my gantry and toolchanger, I decided to tackle the last part of my project: The Z Axis. I first started by drawing out my motor locations in my mastersketch. 

![image](https://github.com/user-attachments/assets/0ccc1654-8180-4c21-a64d-d157e669702a)

Additionally, I had to find my bed. A custom bed or voron type of bed is too expensive for this project, so I found a Railcore 2 Bed for cheap on [Filastruder](https://www.filastruder.com/products/bed?_pos=6&_sid=41451c2f2&_ss=r). 

I then put the bed into my sketch to draw out my total build volume. 

![image](https://github.com/user-attachments/assets/521f28ba-3262-43dc-9913-036a8e47ea36)

The bed is 340mm x 320mm, however, I am going to use a buildplate sized for the K1 Max, so my total build volume will be 310mm x 315mm. 

After I finished deciding on that, I started making my stepper motor mounts for z. I am going with a triple leadscrew kinematic bed mount type of z axis. This means that I have 3 motors on my z axis, and they each individually control one leadscrew. Then, since three points create a plane, a kinematic bed mount is perfect for this. For a better explanation than I could ever make on kinematic bed mounts, see [here](https://3ddistributed.com/corexy-3d-printer/kinematic-bed-mounting/). 

![image](https://github.com/user-attachments/assets/e2e29ed1-fd24-48f7-af15-bda41286d667)

These mounts are simple, but effective. 

Time Spent: 4 Hours. 

## 5/28/2025 Log 12: Kinematic Bed Mounts!

![image](https://github.com/user-attachments/assets/a24e125a-07b8-4411-9760-191e4eeff771)

I decided to make my kinematic bed mounts today. They consist of a magnetic steel ball and a strong magnet, along with a pair of rods to create a joint that is both flexible, yet connected. 

![image](https://github.com/user-attachments/assets/1e0496ac-9dbe-4363-8f06-5a46de119715)

This assembly, one three points, creates a flexible bed that, when properly aligned, stays flat. 

All in all, this kinematic bed mount will also allow the bed to expand and contract as the bed heats and cools, meaning that the bed will not be affected by the heating and cooling cycles, allowing it to stay flat in all conditions. 

Time Spent: 3 Hours
