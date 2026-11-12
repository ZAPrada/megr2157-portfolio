# A10 – Lead Screw Translating System. Ezra Bono & Zachary Prada

# Objective

For this assignment, we were tasked with pairing in groups, in our case: Ezra Bono and Zachary Prada, to design a system which tested materials in tension via a crosshead that was continuously lifted along 2 lead screws. The system needed to be able to pull the material with a repeatable 2000 N of force, have a speed range of 1-50mm/min, be purely mechanical, and have all components designed with a minimum safety factor of 4.

## Lead Screw Calculations (Zachary Prada)

### Lead Screw Diameter 
First we needed to calculate the minimum diameter of the lead screw, to do this we must first list all knowns and unknowns. We would also draw an FBD to go along with this. The yield strength was selected based off of the selection of material avaliable from McMaster-Carr. Specifically 4140 Black-Oxide Steel.

![](A10Z_1.png)

Afterwards we would first find all applicable equations, we would then symbolically solve for our diameter. Once solved symbolically it can be solved numerically, this would leave us with an answer of a minimum diameter of .138 inches.

![](A10Z_2.png)

### Lead Screw Rotational Speed 
To begin, based off of the 4140 Black-Oxide Steel lead screw options available from McMaster-Carr, the smallest diameter lead screw which was still above the minimum diameter previously calculated was 0.25in. Thus, rotational speed would be calculated off of this real diameter in order to get a more real value which our system will experience.

Then we needed to find the rotational speed of the lead screw based upon the linear speed of the crossbar stated in the problem. To do this we started with all knowns and unknowns and drew an FBD to go along with it.

![](A10Z_3.png)

Once all knowns and unknowns are listed we can then find all equations needed to solve for the problem symbolically, after solved symbolically we then solved for it numerically. 

![](A10Z_4.png)

### Lead Screw Torque
To finally pick a lead screw that met all our requirements we lastly needed to solve for out max torque that will be applied on said lead screw. By this point, we had assumed that McMaster-Carr 98940A191 would be sufficient and meet our design requirements. As such, in order to more easily calculate what forces the screw would experience, we decided to use this lead screw in order to eliminate certain variable such as pitch. Then, we listed all knowns and unknowns and drew and FBD. 

![](A10Z_5.png)

![](A10Z_6.png)

After figuring out our unknowns we know what we must solve for, thankfully solving for this problem symbolically was quite easy as there was a readily avaliable formula within the Machinery's Handbook. We then solved numerically to find a max torque of 9.01 in-lbf. Once all our specifications were calculated we then could select an applicable lead screw off of McMaster-Carr-Carr. We finally landed on a 1/4 inch, Black Oxide, Steel Lead screw. (Part Code - 98940A191)

![](A10LS.png)

## Nut and Flange Calculations (Zachary Prada)

We then needed to find a proper nut and flange to go along with our lead screw. To select a proper nut and flange we must perform a stress analysis on the threads. As the interior threads had already been decided (based on the thread spec of the lead screw), we would use ACME 1/4"-16 thread in our analysis. To begin, we: listed all knowns and unknowns, solved symbolically, then finally solved numerically to verify that the interior threads of the shortest nut offered by McMaster-Carr would be sufficient.

![](A10Z_7.png)

A similar process was followed for verifying the the outer threads for the flange to nut connection, but instead with ACME 9/16"-18 threads.

<img src="https://github.com/user-attachments/assets/cde58b69-c5d0-4ced-af09-3943aaf46838" />


Once solved, we then found a nut and flange on McMaster-Carr-Carr that would fit our application, and importantly, worked with our lead screw. (Part Code - 95072A881)

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
| 47065T101 | 4 | [T-Slotted Framing](https://www.McMaster-Carr.com/47065T554) | 11.19 | 44.76 |
| 95082A641 | 2 | [Precision Acme Flange](https://www.McMaster-Carr.com/95082A641) | 37.06 | 74.12 |
| 95072A881 | 2 | [Precision Acme Externally Threaded Nut](https://www.McMaster-Carr.com/95072A881) | 35.78 | 71.56 |
| 98940A191 | 2 | [4140 Black-Oxide Steel Precision Acme Lead Screw](https://www.McMaster-Carr.com/98940A191) | 35.95 | 71.90 |
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

First, using a McMaster-Carr SolidWorks addon, I added in the nut and set its origin to be coincident with the origin of the sub-assembly.

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

### Splitting faces

The faces were split as shown to better simulate how the crosshead would perform under a real test. The square face is where a clamp to hold the material would be attached, while the 2 circular faces are the flange faces.

<img src="https://github.com/user-attachments/assets/5de21ab1-e829-4892-a608-62de1c56ee40" />

<img src="https://github.com/user-attachments/assets/2d2f0f13-d533-4aef-8213-edb8f53593c8" />

<img src="https://github.com/user-attachments/assets/8f6ab67e-9a9c-497d-89f0-c852a152e878" />

<img src="https://github.com/user-attachments/assets/5bb83ab5-95e4-4ce4-aeba-16fcd470a978" />


### Applying forces and Constraining

The circular faces (supporting flanges) were constrained to act as if they were attached rigidly, and the specified 2000 N force was placed on the square face.

<img src="https://github.com/user-attachments/assets/6e05214b-169a-4c8c-98f2-fe966a8dedd6" />

<img src="https://github.com/user-attachments/assets/771e6049-af6a-440f-8b09-d4d47f9581e8" />

### FEA on initial design

First, we did the most course mesh possible to increase compute speed, and analyzed the simulation to find that the part was well within specified design requirements.

<img src="https://github.com/user-attachments/assets/2cf9ae54-cf60-4174-a7ed-c78be410d4ad" />

<img src="https://github.com/user-attachments/assets/d8d7ce17-d7eb-427f-9bd3-1a1370e0cb28" />

<img src="https://github.com/user-attachments/assets/ed24ae34-dc52-4e1c-9c27-cf0895625a7e" />

<img src="https://github.com/user-attachments/assets/758400ed-585c-43e0-b709-a506addc694a" />

<img src="https://github.com/user-attachments/assets/4a2fc0a7-64f3-4ad0-b1a2-4ad208556432" />

 We then ran the FEA again with a finer mesh to test for convergence.

<img src="https://github.com/user-attachments/assets/cadb93bd-abb3-46c8-9ebd-f220ffcb7bed" />

<img src="https://github.com/user-attachments/assets/895df992-5e00-4ef2-a592-fe1a389d730c" />

<img src="https://github.com/user-attachments/assets/8cb9f8fc-e933-454e-bd9d-4fe5152dce86" />

<img src="https://github.com/user-attachments/assets/1add445b-548f-4cc9-a51b-0bcf156efe5b" />

<img src="https://github.com/user-attachments/assets/a485a8c5-1e66-4882-a28e-fcc91bc74bbb" />

<img src="https://github.com/user-attachments/assets/7a227ecc-9b5f-4f39-9932-65efc13f2fac" />

Using these values, we found that convergence was not reached, as such we ran the FEA one last time with the finest mesh possible.

<img src="https://github.com/user-attachments/assets/3d621d8b-7a2e-485b-b3da-8825d598e460" />

<img src="https://github.com/user-attachments/assets/2a098f9d-0573-4d48-9105-406b47361ffc" />

<img src="https://github.com/user-attachments/assets/7384ba5b-2a2a-431f-a099-0a9556975f55" />

<img src="https://github.com/user-attachments/assets/a0726f2f-0202-487a-a3ad-f456c3e75e61" />

<img src="https://github.com/user-attachments/assets/39053f1d-e65f-49b1-8330-831e3ce9dd76" />

<img src="https://github.com/user-attachments/assets/73915536-da7e-48a0-a403-fe06a3feb8ee" />

### Design Alterations & Optimization

As the safety factor was well above the minimum 4 required by the assignment, we chose to alter the design by making the cross sectional area of the crosshead smaller in order to save on material, eyeballing a factor of 1/1.5 derived from guesstimating that we could keep around 2/3rds of the material and still be ok.

<img src="https://github.com/user-attachments/assets/ef47f997-310f-4b94-acd4-be314658adef" />

After we changed the area, we ran the FEA twice again to test for convergence and to see if the crosshead kept a minimum safety factor of 4.

First run:

<img src="https://github.com/user-attachments/assets/aab54d8e-ebce-46d5-a69b-1e652bfa5109" />

<img src="https://github.com/user-attachments/assets/6525f38f-3090-4c94-bae7-2ad96357ba3a" />

<img src="https://github.com/user-attachments/assets/ae2ff6ce-4c66-40d4-a29c-797271d84b3c" />

<img src="https://github.com/user-attachments/assets/492b2516-7ebe-4f47-a7d1-e727cab7c5e6" />

Second run:

<img src="https://github.com/user-attachments/assets/9ed23860-b5e8-4d3d-a322-9d1f2472d0a9" />

<img src="https://github.com/user-attachments/assets/799625de-4014-47f2-90e0-9ec6424605fa" />

<img src="https://github.com/user-attachments/assets/1f961c41-0d19-4def-99f8-eb48e352f853" />

<img src="https://github.com/user-attachments/assets/9eb31d31-c3b9-43fb-896f-dd7ca02ef88a" />

<img src="https://github.com/user-attachments/assets/e657c68f-38bb-4e5a-b488-c7be0731ea35" />


Calculating the difference in these simulated values, we found that they do not converge to less than 7%, as such we ran the FEA one last time, again at the finest mesh setting allowed by SolidWorks.

<img src="https://github.com/user-attachments/assets/c376c0dd-a38f-4e11-a30b-40b0bc694b39" />

<img src="https://github.com/user-attachments/assets/6fd2b41d-2361-4b37-86ad-9577fb0ea789" />

<img src="https://github.com/user-attachments/assets/de1956c8-7c72-459b-bc89-bdeb339addc3" />

<img src="https://github.com/user-attachments/assets/42e0e1d4-5353-4ffa-8e16-5ba07b0fcdc9" />

<img src="https://github.com/user-attachments/assets/9b62ea48-a9ab-45a2-83d3-8e3b3ab23e7f" />

<img src="https://github.com/user-attachments/assets/934673b5-66cf-412e-8b0f-1d3debdc6ab8" />

At this finest mesh setting, we found that the minimum safety factor was just over 4, right on the line of what is acceptable by the assignment, and thus a design that has been optimized primarily for mass.

Mass before: 3.11 lbs

<img src="https://github.com/user-attachments/assets/1619e066-c648-49f9-a910-d44c066b53fb" />

Mass after: 1.38 lbs

<img src="https://github.com/user-attachments/assets/30f42c32-9870-444f-bfe9-e8b5238b80a2" />



### Crossbeam Drawing

<img src="https://github.com/user-attachments/assets/f627cf13-e9b0-447e-87b3-18f8fc1b9c56" />


## CAD Files download

[Click Here](https://drive.google.com/file/d/1OajoFGYmqYE4BQru5pYw5TExjGy32nfQ/view?usp=drive_link)
