D# A10 – Lead Screw Translating System

# Objective

For this assignment, we were tasked with pairing in groups, in our case: Ezra Bono and Zachary Prada, to design a system which tested materials in tension via a crosshead that was continuously lifted along 2 lead screws. The system needed to be able to pull the material with a repeatable 2000 N of force, have a speed range of 1-50mm/min, be purely mechanical, and have all components designed with a minimum safety factor of 4.

## Lead Screw Calculations (Zachary Prada)

### Lead Screw Diameter 
First we needed to calculate the minimum diameter of the lead screw, to do this we must first list all knowns and unknowns. We would also draw an FBD to go along with this. The yield strength was selected based off of the selection of material avaliable from McMaster. Specifically 4140 Black-Oxide Steel.

![](A10Z_1.png)

Afterwards we would first find all applicable equations, we would then symbolically solve for our diameter. Once solved symbolically it can be solved numerically, this would leave us with an answer of a minimum diameter of .138 inches.

![](A10Z_2.png)

### Lead Screw Rotational Speed 
To begin, based off of the 4140 Black-Oxide Steel lead screw options available from McMaster, the smallest diameter lead screw which was still above the minimum diameter previously calculated was 0.25in. Thus, rotational speed would be calculated off of this real diameter in order to get a more real value which our system will experience.

Then we needed to find the rotational speed of the lead screw based upon the linear speed of the crossbar stated in the problem. To do this we started with all knowns and unknowns and drew an FBD to go along with it.

![](A10Z_3.png)

Once all knowns and unknowns are listed we can then find all equations needed to solve for the problem symbolically, after solved symbolically we then solved for it numerically. 

![](A10Z_4.png)

### Lead Screw Torque
To finally pick a lead screw that met all our requirements we lastly needed to solve for out max torque that will be applied on said lead screw. By this point, we had assumed that McMaster 98940A191 would be sufficient and meet our design requirements. As such, in order to more easily calculate what forces the screw would experience, we decided to use this lead screw in order to eliminate certain variable such as pitch. Then, we listed all knowns and unknowns and drew and FBD. 

![](A10Z_5.png)

![](A10Z_6.png)

After figuring out our unknowns we know what we must solve for, thankfully solving for this problem symbolically was quite easy as there was a readily avaliable formula within the Machinery's Handbook. We then solved numerically to find a max torque of 9.01 in-lbf. Once all our specifications were calculated we then could select an applicable lead screw off of McMaster-Carr. We finally landed on a 1/4 inch, Black Oxide, Steel Lead screw. (Part Code - 98940A191)

![](A10LS.png)

## Nut and Flange Calculations (Zachary Prada)

We then needed to find a proper nut and flange to go along with our lead screw. To select a proper nut and flange we must perform a stress analysis on the threads. As the interior threads had already been decided (based on the thread spec of the lead screw), we would use ACME 1/4"-16 thread in our analysis. To begin, we: listed all knowns and unknowns, solved symbolically, then finally solved numerically to verify that the interior threads of the shortest nut offered by McMaster would be sufficient.

![](A10Z_7.png)

A similar process was followed for verifying the the outer threads for the flange to nut connection, but instead with ACME 9/16"-18 threads.

<img src="https://github.com/user-attachments/assets/cde58b69-c5d0-4ced-af09-3943aaf46838" />


Once solved, we then found a nut and flange on McMaster-Carr that would fit our application, and importantly, worked with our lead screw. (Part Code - 95072A881)

![](A10NF.png)

## Crosshead Calculations (Ezra Bono)
### Stress Analysis 
The first thing we must calculate for our crosshead is the max stress applied on the bar, when at a max load of 2kN. We must to this to figure out how thick we must make our bar to not snap under load. Firstly we made a few assumptions, we decided on a square cross-section as it's much easier to calculate and when assembled it less complex to manufacture and assemble. Our second assumption is that our material is ATSM A36 Steel, we choose this material due to wide use already in many applications that involve beams with a point load on them, our second reason for choosing is that it is readily available. The first step we did to solve for the max stress was to list all knowns and unknowns and drew and FBD to go along.

![](A10_1.png)

Afterwards we listed all equations and then solved for the side length symbolically, once symbolically solved we then solved for it numerically. Doing so gave us a minimum side length of 31 mm.

![](A10_2.png)

### Deflection Analysis
The next thing to solve for the max deflection on the beam. We were given a hard limit of no more than .1mm deflection. To find the minimum size needed to achieve this we first listed all knowns and unknowns and drew and FBD.

![](A10_3.png)

Once all variables were listed, the next step is to list all equations and solve symbolically. Once solved symbolically we solved for side length numerically giving us a final side length of 21.27mm.

![](A10_4.png)

Since our minimum side length of our stress analysis was higher than the minimum side length of our deflection analysis we must use a side length of 31mm or greater. Taking this into account we have a beam that is 127mm long and is 31x31mm wide, two holes are drilled into the bar to fit both of the lead screws, each being at 7.62mm.

![](A10_5.png)


## BOM for complete system (Ezra Bono)

| Part Number | Quantity | Name | Unit Cost | Total Cost |
| :--- | :--- | :--- | :--- | :--- |
| 47065T101 | 4 | [T-Slotted Framing](https://www.mcmaster.com/47065T554) | 11.19 | 44.76 |
| 95082A641 | 2 | [Precision Acme Flange](https://www.mcmaster.com/95082A641) | 37.06 | 74.12 |
| 95072A881 | 2 | [Precision Acme Externally Threaded Nut](https://www.mcmaster.com/95072A881) | 35.78 | 71.56 |
| 98940A191 | 2 | [4140 Black-Oxide Steel Precision Acme Lead Screw](https://www.mcmaster.com/98940A191) | 35.95 | 71.90 |
| **Total** | | | | **262.34** |

## System CAD Model (Zachary Prada)

### Crosshead Design

As the crosshead needed to be designed, we first began by creating a set of variable in SolidWorks based off of previously calculated values. The extra length variable was made to allow for material around the lead screws which would be inserted into the crosshead.

<img src="https://github.com/user-attachments/assets/7504505e-30a5-4dcd-a750-98f9b4d4c435" />




Then, as the cross section of the crosshead was calculated as a square, I created a sketch of a square which had side lengths defined parametrically while also using relationships to keep definitions to a minimum.

<img alt="image" src="https://github.com/user-attachments/assets/05afb281-4357-466b-8e88-d4e1834cb0ab" />




Then, using the symmetry of the crosshead, I only extruded one side then would later mirror the features to complete the other.

<img src="https://github.com/user-attachments/assets/1fdf090c-f8fb-4ee1-aedf-a4ec74ff970b" />


I then created a point which was defined as the extra length away from the center of the edge, from which I placed and threaded a hole to model the threads with which the lead screw would pass through. 

<img src="https://github.com/user-attachments/assets/b4bf3917-613e-4e1f-a1e4-501791a00c3a" />

<img src="https://github.com/user-attachments/assets/dbc10455-4671-426e-b44c-ab23749734dd" />

<img src="https://github.com/user-attachments/assets/820cf13d-a37f-49fb-a8fe-89b324b33357" />


After all the features on one side were modeled properly, I then mirrored all the features to complete the other side of the crosshead

<img src="https://github.com/user-attachments/assets/5fdc6422-2251-42b1-b2ef-1eb3e41e2701" />

<img src="https://github.com/user-attachments/assets/8d6cf2ff-6ab4-4499-84db-724ec3ce7239" />


### Nut and flange sub-assembly

In order to make the final assembly simpler, I chose to have the nut and flange be made into a subasssembly that would then be put into the larger main assembly.

First, using a McMaster SolidWorks addon, I added in the nut and set its origin to be coincident with the origin of the sub-assembly.

<img src="https://github.com/user-attachments/assets/91a36d06-b80c-405d-85cc-8b9e6a301bf1" />

<img src="https://github.com/user-attachments/assets/f9be8390-4854-471d-baab-ee14c2755a46" />

<img src="https://github.com/user-attachments/assets/1ff8a0b5-eb75-4c1d-ad9a-6415c5561680" />


I then imported the cheapest flange which had threads which would fit the chosen nut, and attached it to the nut using mates.

<img src="https://github.com/user-attachments/assets/7e16672f-a3aa-4386-bd34-71352ba52bd5" />

<img src="https://github.com/user-attachments/assets/5f785362-918c-4b9d-a81a-9e2a9e7b907d" />

<img src="https://github.com/user-attachments/assets/92d9f73b-8e2c-44e3-8b13-9e3d11ef5fd9" />

<img alt="image" src="https://github.com/user-attachments/assets/3db99af2-e1b8-45fd-98e3-d671fdb898ea" />

After I had finished with this sub-assembly, I went on to begin the primary assembly

### Main Assembly

First, I imported the crosshead, and set its origin to be coincident with the origin of the assembly, so that I would have a good center to work off of.

<img src="https://github.com/user-attachments/assets/d14d4e51-8bd1-4c67-a7c1-5739d57659ff" />


I then imported the chosen lead screw, made it concentric with the threads in the crosshead, and set it to be roughly centered with the crosshead so the entire assembly could easily fit on screen.

<img src="https://github.com/user-attachments/assets/c83f9d15-4eab-4b72-aeb7-b78ba0d7e0e9" />

<img src="https://github.com/user-attachments/assets/33180bd9-a4fa-4e5f-8a1a-00ad9d39c5e7" />

<img src="https://github.com/user-attachments/assets/21dae8b2-fe08-4de9-a3bc-566b716b0a87" />


Then, as the crosshead was symmetrical, I used the mirror component tool across the midplane of the crosshead in order to simply the assembly process.

<img src="https://github.com/user-attachments/assets/e9ff6afa-1332-44fa-9585-fe60f07ab8c1" />

<img src="https://github.com/user-attachments/assets/30ffa83e-3f5a-4566-9449-c78393b689cf" />

Then to create the frame. I imported 4 T-slotted frames and aligned them with the lead screws using mates to allow for consistent locations even if things were to move, mirroring vertically using a midpoint plane set between the top and bottom of one of the lead screws, and mirroring horizontally using the assembly's horizontal midplane to again, save on modeling time.

<img src="https://github.com/user-attachments/assets/05ddf9db-2223-4fed-a935-637918ff4cb1" />

<img src="https://github.com/user-attachments/assets/4ef3477a-98e9-40bf-8508-baf78c2e761f" />

<img src="https://github.com/user-attachments/assets/bb869542-3eaa-4064-8c5d-7617e2f92da5" />

<img src="https://github.com/user-attachments/assets/89a5b0cf-88fc-4bd8-bc1b-4ad88b6ed2bd" />

<img src="https://github.com/user-attachments/assets/d3f33f9c-ef66-47c3-ac63-a4eb7c0433b2" />

<img src="https://github.com/user-attachments/assets/ce743e58-3bce-487f-bcab-e36902decfc2" />


Creating the aforementioned midplane and mirroring the bottom frame.

<img src="https://github.com/user-attachments/assets/8e993e99-7da0-44d7-9cbe-724cb771c27a" />

<img src="https://github.com/user-attachments/assets/d96dc792-2718-4b69-98cd-564aae07de57" />

<img src="https://github.com/user-attachments/assets/2c4407d5-7a67-4eba-9f10-d157d8a2c905" />



Importing and placing the vertical frame pieces.

<img src="https://github.com/user-attachments/assets/e573f265-25ce-4635-bfa6-84c0a93a99d4" />

<img src="https://github.com/user-attachments/assets/3effc7e5-0fd0-41b0-98b5-e6e298842a99" />

<img src="https://github.com/user-attachments/assets/dc3f6e11-3649-4055-987d-6cc2d64eb1fc" />

<img src="https://github.com/user-attachments/assets/614d01e6-beea-4836-a278-70f5f43f6d6f" />

<img src="https://github.com/user-attachments/assets/d81fbde6-3e68-48b3-8370-290775b57757" />

<img src="https://github.com/user-attachments/assets/0488f652-fd73-4707-b6a9-fb0f184c3368" />


I then imported the previously created nut-flange sub-assembly and made the interior of the threads of the nut concentric with the threads, and placing the flange face on the bottom of the crosshead to better support the crosshead when tensioning a material.

<img src="https://github.com/user-attachments/assets/77d11381-511b-4243-8a1f-151415480b76" />

<img src="https://github.com/user-attachments/assets/a730102b-d2ed-4cbe-b8a2-5f8b32b531fe" />

<img src="https://github.com/user-attachments/assets/ec031012-9044-4262-85e8-ae5fd8f8f94b" />


I then repeated the process a other lead screw, importing a copy of the nut-flange sub-assembly.

<img src="https://github.com/user-attachments/assets/54f2d825-4682-45c6-af55-170aec29f2cc" />

<img src="https://github.com/user-attachments/assets/bf179d72-a8be-4fba-aae3-fa9e6824e9f3" />


Completed assembly:

<img src="https://github.com/user-attachments/assets/acb1a15e-ccb3-404a-a9b0-59bec8b015f3" />


## Reflection (Ezra Bono & Zachary Prada)

An engineering lesson we both learned while working on this project is that playing to others strengths is incredibly beneficial to effeciancy of a project. As Ezra is more experienced with solids, he oversaw the work done in hand calculations, while Zachary is much more experienced in SolidWorks, and thus was in charge of the CAD modeling. With this division of responsibilities, we were more able to more effectively complete the project as a whole, while simultaneously learning skillets from each other.

In total, this assignment took 12 hours to complete.

## 2157 Specific Section (Ezra Bono)




































## Decide


## Communicate


