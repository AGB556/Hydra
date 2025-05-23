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

## 5/22/2025 Log 6: Toolhead

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

## 5/22/2025 Log : Toolhead CAD

I started to put my ideas for the toolhead into cad. Here is the general idea behind my toolhead.

![image](https://github.com/user-attachments/assets/039f03df-eeb1-46a0-9f87-fe4ff5aef5dd)

WIP
