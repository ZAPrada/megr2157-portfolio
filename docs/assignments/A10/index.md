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


I then created a point which was defined as the extra length away from the center of the edge, from which I placed and threaded a hole to model the threads with which the lead screw would pass through











## Decide


## Communicate


