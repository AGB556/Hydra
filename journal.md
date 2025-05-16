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
