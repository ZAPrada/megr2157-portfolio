# A4 – [Topic]

## Objective

For this assignment, I was tasked with designing a motor mount optimizing for maximum stress, and then a maximum deflection 0.30mm, and then picking the design which is able to meet both requirements.

## Analyze

To begin with, I first began by taking note of what all my constraints were. I first turned towards the motor to see what would be the dimensions I would be working around. Thankfully, the motor provided in the assignment came with a fully dimensioned drawing, greatly simplifying later design.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/aad7d014-a84b-4657-a72f-7de31770e374" />


I then needed to analyze the design constraints put on me by the assignment. The motor was to be mounted on an L shaped mount, which completely contains the motor, with one "stick" of the L rigidly attached to a wall, and withstand a 300N of force acting on the very tip of the motor shaft. As the assignment directions specifically stated to ignore the weight of the motor, for my calculations I would not take into account what orientation the motor would be mounted in, assuming it to essentially be in zero-gravity. 

<img width="500" alt="image" src="https://github.com/user-attachments/assets/c0775a20-70a1-4ccb-a4ed-55a472d7a835" />


The assignment gave us a total of 3 material to make the mount out of: ABS, PETG, and PLA. I then looked through each of the 3 options (which were in reality 2 as the link for PETG was dead) and compared and contrasted their material properties. Unfortunately however, I found the information in the links provided very confusing and thus opted to instead go with the material I was the most familiar with: [PLA](https://www.matweb.com/search/DataSheet.aspx?MatGUID=ab96a4c0655c4018a8785ac4031b9278).

<img width="500" alt="what even is all of this" src="https://github.com/user-attachments/assets/00fcbda1-9df9-4c66-a979-a52decfdaf98" />


After having chosen my material, as per the assignment instructions, I did some surface level research on what types of mounts already existed for similarly sized motors on large online retailers such as Amazon, Walmart, and AliExpress, as I believed that mounts such as these were a solved problem, and the "best" general shape had already been found and was able to be produced on such mass scales. In my research I found 3 good examples for which I would base my own design off of:


[One mount sold on Amazon](https://www.amazon.com/dp/B0C8GHQRY5?ref_=cm_sw_r_cp_ud_dp_CN012HJFBZV7BZYCFCCA)

<img width="500" alt="image" src="https://github.com/user-attachments/assets/8a539fb7-4c61-49e5-b681-d4984f3ea2ab" />



[One sold at Walmart](https://www.walmart.com/ip/CHANCS-Brush-Small-DC-Motor-12V-24V-DC-775-Motor-6000RPM-12000RPM-with-Bracket-Set-for-Electrical-Tools-DIY/19636174261?classType=VARIANT)

<img width="500" alt="image" src="https://github.com/user-attachments/assets/57a5a817-0b66-4c84-8fe2-6dd13e4bea1f" />



[And one sold on AliExpress](https://www.aliexpress.us/item/3256806524266816.html)

<img width="500" alt="image" src="https://github.com/user-attachments/assets/a86af851-d3e8-4b28-8d2e-66cae3649625" />


## Mount Design

Based on the 3 mounts researched, I sketched up a general design for my mount, where the motor's face would mount into the upright T section, and the base B would be attached to a rigid surface with only 2 screws, as it appeared that >2 would use more resources than necessary.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/029e5e08-7167-47e6-8cc8-7287c0c64293" />


### Hand Calculations

I began the number crunching by first simplifying the forces experienced by the mount so they could fit easily into the formulas provided by the Machinery's Handbook. To do this I took the force put on the tip of the motor shaft and imagined it pulling the entire motor forward, thus changing the point force into a distributed force along the face where the motor would sit.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/12d45d71-9d98-4d58-988c-0eeba0428f54" />


After simplifying the force applied to the T section of the mount, I then (as per the image above) sectioned off the T section and imagined the B section as rigid, thus turning the T section into a cantilever.

Before doing any math however, I went through and noted all my known and unknowns.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/df16801b-d007-4af7-b579-0aeefbee4bdb" />

While finding these values though, all of the listed values were given by either the assignment, or by the "average value" given in [this data sheet for PLA](https://www.matweb.com/search/DataSheet.aspx?MatGUID=ab96a4c0655c4018a8785ac4031b9278). However, the volume of the T section was not given, and as there were 3 variables, I was going to need to fix 2 of them as there was no easy way to setup a system of equations for even 2 variables (despite my multiple, multiple attempts to do so). Thankfully however, the dimensions of the motor eased restraining the length and thickness of the T section. 
The length I chose as equal to the highest outside diameter of the, plus a tolerance of 3mm on each side, equaling a final diameter of 34mm, 6mm oversized from the outermost point of the motor, ensuring the motor could be fully encased in the mount.
The thickness ("height") was similarly simple to find. I took the difference between the length from the tip of the motor shaft to the face of the motor and the end of the key for the motor shaft (the 2 circled dimensions), ensuring that the motor would be able to mount to as much material as possible without shortening the working length of the motor shaft.

<img width="365" alt="image" src="https://github.com/user-attachments/assets/db77adb2-26c4-44c0-b95a-90480ca05041" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/2e06d500-8de3-41af-b171-81bd99b48782" />


With now only 1 unknown left, the width of the mounting face _b_ (technically 3 as the section modulus and moment of inertia include the last unknown _b_ in their formulas and thus are technically unknown), we can use the equations for maximum stress and maximum deflection, solving for b, and picking the higher b value to ensure that we can meet both requirements.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/cd03c38f-0427-4994-9d91-598bbdf73673" />


As per the calculations, a width of 116mm will make sure the T section does not go past its maximum allowed stress, nor its maximum allowed deflection.



The process for finding the required geometry of the B section is similar, but requires a different setup. I first assumed (to make calculation easier) that the P force would translate through the T section and act as a point force at the tip of B. Secondly, as the B section is held in with screws, the actual length that can deform is all the material _after_ the first screw, as such I setup the FBD of the B section to be a cantilever mounted where the screw holds the section down, with a force P acting on the section at its tip.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/063e9982-f7fb-4392-ae7c-c7c9029d2583" />


With this setup we can go through the same process as before, though this time choosing different variables to fix/leave independent. Firstly, the width of the B section had to equal the width of the T section otherwise the T section would not work as calculated. Secondly, I chose to keep the thickness the same as the T section mainly for aesthetic reasons, as having a thick base compared to the mounting face could setup strangely if this were to be used in an actual project. Thus the only independent variable left was the length L of the B section from the point of the first bolt/screw to the tip.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/86086b9a-be70-4fec-92a4-45e7ea1bae4e" />


Similarly with before, solving for the maximum deflection gives us a higher value for out solved-for variable, thus L will be set to 27.4mm to ensure that the B section can meet both its strength and deflection requirements.

## Cad modeling

Although I had done all the calculations by hand and determined all the values for the geometry of the mount, I still chose to solve for them parametrically, as if this were a real part and put into the real world, I would need to be able to easily make edits to the geometry based on how part testing goes. 

<img width="679" height="194" alt="image" src="https://github.com/user-attachments/assets/f1f1c071-5fc1-4ec8-bfee-f0ed9cd0a900" />


With all my parametric variables and equations sorted out, I could begin modeling, first by creating a sketch for the main area of the B section, making sure that the dimensions are referencing my parametric equations. For the length dimension, I added 10mm (using an equation in the dimension) to the previously calculated value to allow room for the bolt that was ignored during my calculations.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/b2e58c7f-11cb-4b8f-9f6b-94544f9defb1" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/a3cdaa85-333e-4f68-89ef-a1fb08119115" />



Extruding section B to the previously decided on thickness.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/7ecdcd70-d6a2-4f04-bf1e-724af975db3b" />


Then making another sketch for the T section on the rear face of the B section, making sure that I set the height to start at the top of the B section by using coincident relations.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/9dc1c0e7-b59f-4068-85d1-dd6b3df6f42c" />


Extrude to the previously calculated thickness.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/304faec1-3bd5-42be-84a0-b4ce8e93334e" />



I then began to model the hole where the motor shaft and the 2mm protrusion of the motor would sit. For these I attempted to use the hole wizard to allow for easier future modifications, however I could not get the hole wizard to give me the required dimensions. As such I needed to make circle sketches and cut extrude them. To further simplify the dimentions, I chose to locate these holes in the exact center of the T section inside face using centerlines and multiple point relations.


Dimensions to be cut

<img width="500" alt="image" src="https://github.com/user-attachments/assets/8f7130b0-2d1e-4f9b-9b46-31a894ab513d" />


Cuts

<img width="500" alt="image" src="https://github.com/user-attachments/assets/5b87e777-4362-4a4b-9339-6244ebac9be8" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/676a8221-5526-4221-9076-3317a0b2d62a" />



Thankfully for the motor mounting bolt holes (required to be Ø3.4 mm clearance holes as per the assignment instructions.) I was able to configure the hole wizard to automatically sketch and cut exactly the required clearance hole to allow for an M3 bolt to pass through, only needing to make 1 sketch defining the radius of the bolt circle..

<img width="500" alt="image" src="https://github.com/user-attachments/assets/d3ebba90-0661-4051-8d48-3fe94df92702" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/0ec9744f-9961-4299-a478-0f6e5e95f88d" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/1cf47479-fbac-44c9-841b-c22142fd3d1c" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/c6340fbe-a0c8-40f2-9573-43c3968e201c" />



After I created this one hole using the hole wizard, I let solid works create the other 3 I needed to the same specifications by using the radial pattern tool on the clearance hole, making  sur its axis of revolution was the 2mm countersink it would always be concentric with. 

<img width="500" alt="image" src="https://github.com/user-attachments/assets/2807ff7c-6c5c-46dd-831a-0156bf84fa83" />



Finally, the 2 hold with which bolts will mount the mount to a rigid surface were able to be made with the wizard tool, also allowing for the exact same specifications as the previous 4 holes. As with before, I needed to create a sketch which included a point to where I could tell the hole wizard to make the hole.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/df414408-2e76-48c1-8441-d0ba9ed2b58c" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/8a6d6ab7-4cef-4bf1-a247-680823615e80" />



Very lastly, as the mount is symmetrical across the x-axis, to replicate the B section clearance hole on the other side, thus giving me my 2 bolt minimum, I simply used the mirror tool across the XZ plane to ensure if I would only ever need to change the location of one hole and still be able to keep perfect symmetry.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/3973ab04-c164-450b-8dec-4d76e1cc720e" />


#### Finalized Part with download

<img width="800" alt="image" src="https://github.com/user-attachments/assets/d4c3a80d-85d3-43bf-9518-4b598862df20" />


[Download](https://github.com/user-attachments/files/32326118/Part2.zip)


## Reflection

The hardest part of this assignment easily was understanding how the part would deflect and how to apply the formulas learned in class. Even with help from a friend who is very good at solid mechanics, it still took me several hours of studying and research (and ultimately guess work) to understand how the force and motor would interact to deflect the beam. In the end I honestly do not believe I did it correctly, but this experience was very valuable in allowing me to find gaps in my knowledge.

In all this assignment took me 20 hours to complete.

## 2157 Specific section

<a href="https://github.com/user-attachments/files/32326328/A4.pdf"><img width="900" alt="Part2" src="https://github.com/user-attachments/assets/a93380af-5974-4ecf-bdeb-8e8d3c8ce690" />

Click image to download as PDF.


To download and view in SolidWorks, [click here](https://github.com/user-attachments/files/32326118/Part2.zip).
