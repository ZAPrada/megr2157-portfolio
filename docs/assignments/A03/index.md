# A3 – Parametric Design Optimizing for Strength

## Objective

For this assignment, I was tasked with designing a cantilever bar with a circular cross section that, when in axial tension, would not stretch (deflect axially) more than 0.009in. The bar had to be made out of aluminum and had to withstand an axial tension load between 300 and 500 lbs. The main point of this assignment was to design this bar within CAD using parametric values. Essentially, only imputing a few variables, and then setting up equations with those variables, and then driving the dimensions of our bar based off of those materials. After our bar was designed, we were to conduct a Free Element Analysis using CAD to determine if, based off of our calculations, we had designed the bar correctly. 

## Hand Calculations

To begin with I needed to understand how the bar was expected to be loaded and setup, and after some time reading through the assignment instructions, I had come to the conclusion that it was to be a cantilever pulled along its axis by some force.

<img width="500" alt="FBD of bar" src="https://github.com/user-attachments/assets/03a3bc5b-eab0-4192-a1b3-b9d5f9c80f51" />


After noting how the bar was to be setup, I then went about figuring out the math which I would use to design the bar. As per the instructions, I went with direct tension elongation equation found in our Machinery's Handbook. This equation relates axial stretching (*e*) to force (F), length of the bar (L), cross sectional area of the bar (A), and the modulus of elasticity of the material the bar is made out of (E).

<img width="500" alt="image" src="https://github.com/user-attachments/assets/4c0b1ae8-924e-47ce-b2a5-31e8f6a275b1" />


After picking this equation, I then went about noting which values I did and did not know. 

Firstly, my knowns: I was given maximum axial deflection from the assignment instructions (0.009in), thus I set my value for *e* to 0.009 as when I went to solve for an unknown, it would give me the minimum value for that unknown which would meet the requirement of not stretching more than 0.009in. I then set my applied force to be the maximum given by the assignment, 500lbs, to again, let my unknowns be the smallest they could be to ensure my final bar would be able to withstand the maximum load it may see. For my modulus of elasticity, I turned to SolidWorks to give me that value so that way my hand calculations would be accurate to my FEA. Picking **3.0205 (EN-AW 1200)** aluminum (99.5% pure aluminum) as my material in SolidWorks gives me an E of 10152641.64 psi. 


SolidWorks aluminium

<img width="500" alt="image" src="https://github.com/user-attachments/assets/d52074d7-3e2a-471e-827f-e430b4a7517a" />


As for my unknowns: I had the length of the rod (L) and its cross sectional area (A). As I had 2 unknown and only 1 equation, I wouldn't be able to create mathematically perfect bar given the specifications, as such I was going to have to solve for one variable and then choose a value for the other variable. After doing the algebra and solving for both variables, I decided on letting the length be the function of the other variables, and picking a value for A as the equation when solved for length was much more simple and neat.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/eea06642-afa2-4a9f-a92e-d1e4c81c8694" />


After getting my hand calculations and algebra set in order, I was ready to move onto the CAD phase of the design.


## Parametric Design in SolidWorks

I then opened SolidWorks, created a new part, and then began typing in all my previous known variables and defining them to the same letters they had before, except for *e* which I had to change for *s* as SolidWorks considered *E* and *e* to be the same letter. As I had to pick a value for A, which actually was picking the value of the diameter of the circle as that's how the circle from which I would extrude my rod would be defined, I chose my value of 3in at random believing it would produce an adequate rod.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/b127d6a8-0467-4923-9fb2-78be04bf5811" />


I then started a new sketch, and made a center point circle and defined its diameter as my variable *d*.


<img width="500" alt="image" src="https://github.com/user-attachments/assets/73783821-faa0-4840-8bfe-cad38d50a250" />


I then extrude the sketched circle out setting its length to the parametrically determined length *L*

<img width="500" alt="image" src="https://github.com/user-attachments/assets/4170595d-9e8a-4643-aa69-013705ecc1dd" />


It was at this point when I realized my parametric calculations had given me a length of 1614in, or 134.5ft, or about 13 stories long. Believing this length to be way over what was "correct," I then went over my math several times, even checking the parametric calculation by hand, but all the numbers and concepts seemed to line up. I however still felt that a length of a highrise building for a 3in wide rod was way over what I was *supposed* to have. So I then contacted my Structural Engineer friend who knows much more about solid mechanic than I do and asked for his advice. After some conversation, he explained to me that I had chosen an extremely high value for my diameter, reminding me about how well metal is at resisting elongation, and pointing out how absurd a 3in thick piece of metal would need to be for it deflect even 0.009in. After selecting a smaller diameter value of 0.5in, my final rod was much more reasonable in size.


<img width="500" alt="image" src="https://github.com/user-attachments/assets/47111f0f-5a09-464a-80e5-bf42df7b2ab8" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/e23c8a03-0710-4dc2-8f63-cf1d845d0ea7" />

Much more reasonable size.

As I had to lookup materials to get the modulus of elasticity for my *E* value, I then went back to the SolidWorks Materials menu and selected the same spec of aluminum as my modulus of elasticity, and applied it to my model.

## FEA

Once my rod was designed, conducting the FEA was as simple as following the video tutorial provided in the assignment directions.

First, I went to the Simulation tab in SolidWorks and set it to a Static study.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/fb8cc9b7-81d1-43e2-97df-56b21c729a24" />


Set the point of the cantilever that would be fixed in place ("against a wall"), which would just be one of any of the 2 circular faces.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/eaedbae1-1d09-4039-9c01-aa151438d141" />


Choose the end which would have the 500lb axial tension force applied to it, which would be the opposite circular face that would be the mount of the cantilever.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/49d81b7b-5efd-4fbd-a782-ae8cf3828b4a" />


Pen-ultimately, create a mesh with medium resolution for the object so that SolidWorks would be able to efficiently, but accurately, calculate the stress and stretch on the rod.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/b84a821b-0fef-494c-9838-9114db1c5000" />


Lastly, run the simulation and observe the results for displacement.


#### Deflection Map

<img width="500" alt="image" src="https://github.com/user-attachments/assets/8e151cee-a4e1-47f5-a470-3cebf7296fcf" />


#### vonMises Stress Map

<img width="500" alt="image" src="https://github.com/user-attachments/assets/7baf9934-5901-4d89-bbf7-08790e672f22" />


Pulling from the data of the 99.5% pure aluminum in SolidWorks, aluminum has a yield strength of about 40,000 psi (40 ksi). My rod however, based off of the vonMises stress map, sees a peak of 3626 psi (3.6 ksi). Rearranging the formula for working stress to solve for safety factor, I found my safety factor to be a whopping 11.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/833bf791-5e1c-448e-b679-a8192bcc7d01" />

## Reflection

Upon viewing the axial displacement of my rod in the deflection map, we can see it has a maximum value of 0.009005in, meaning the % difference between my read value and the maximum allowed displacement is a solid 0%, in other words, exactly as calculated. Based on this information we can infer that a circular, pure aluminum rod, has a minimum diameter of 0.5in and a minimum length of 35.88in if the design requirement states that it cannot stretch more than 0.009in. These numbers are not surprising as my calculations for the length were dependent on the maximum allowed stretch. So it is fully expected that a rod with these dimensions would meet the design criteria, even though it is meeting them at the extreme.
Additionally, though the stress that the aluminum sees is much less than its yield strength, as the design requirements state that the *maximum* allowed stretch is 0.009in, I would prefer a design that had a thicker diameter, so that the extra molecular bonds withing the thicker rod would increase its overall strength, making sure that when >500lb of force is applied to the rod in tension, it will never get near that 0.009in stretch figure.

### Same rod, now with a hole

The end of the assignment description states that I must imagine a large hole on the mounting side of the cantilever, and estimate the stresses around the hole and be sure that they do not exceed my safety factor of 11.

Firsly, as these values are typically found through testing, I needed a graph showing me the relationship between the size of the hole, and its related stress concentration factor, on a rod in tension. I was able to find as such in a Mechanical Engineering Design textbook written by Peterson which states exactly what I needed.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/cebf46c5-e0cd-4966-aa18-8b8162b3c2c5" />


Given that the assignment directions ask for merely a "substantial pin hole," I chose my pin hole to take up half of my rod's diameter, giving me a value of 0.5 on the x axis. Then, tracing the graph, I get a value of about Kt = 2.2. Using this value, and the stress value read from my vonMises stress map close to the mounting point, I was able to use the Stress Concentration factor formula found in the Machinery's Handbook, along side the working stress formula, to roughly estimate what the stresses in the portions around the hole would be.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/1d4dae9e-1cbc-4522-868c-908f274ba7dd" />

I chose a value of q = 0.05 as Machinery's Handbook says that ductile material have a q = 0, and while aluminum is a ductile material, if I were to set K = 1, my results would be meaning less as the value calculated for stress around the pin hole would be the same as if the hole were not there, which is never the case in reality. As such I decided to pick a very low value so that sounded reasonable so that way my calculations would preform in some measurable way.


With this stress around the hole calculated, I was able to then recalculate what my maximum allowed stress is based off of my previously calculated safety factor.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/eab9ee90-4108-4650-b017-f0801ad33108" />

As such, a pin hole diameter must be less than half of that of the diameter of the rod, otherwise the stresses around the pinhole exceed that of my safety factor's acceptable max, which could lead to a catastrophic safety failure if too much load is put on the rod. 


## Lessons Learned

Compared to the previous assignment, I was glad this task didn't need nearly as much Solid Mechanics knowledge to accurate perform, as well as much less hand calculation. I much enjoyed how the only real math I have to do by hand for designs such as this is simple algebra, and I can simply input the values into SolidWorks and have it do the hard math for me. When learning how to setup equations within SolidWorks however, I found that you need to be very specific in how you define things, otherwise your dimention may only pull and set the value of the variable, instead of constantly pulling the value from the equations table. Additionally, I learned that you must have a firm grasp of how materials handle and their expected weakness and strength and how those weakness and strengths relate to their size, otherwise you may accidentally over-design a part by several orders of magnitude and cost the company you work for millions in unnecessary cost.

In total I spent around 6 hours on this assignment.

## 2157 Specific Section: Modifying Design Parameters.

Through my conversation with my structural engineer friend, and viewing my parametric equations, I believe:
1. If I were to change only the diameter of the rod, my final axial stretch would be the same, as the same load is applied and my length is based off of my diameter, causing the relationship between the diameter and the length to stay constant.
2. If I was to change the the *expected* load (F) to a higher value, keeping all other variables equal, my final axial stretch would be less than 0.009in, as I had effectively designed the rod to withstand a higher load than it would be seeing during the FEA.
3. If I were to keep all other variables equal, and only increase the length of the rod, I believe that the rod's final axial length will decrease, due to the fact that there are more atomic bonds resisting the stretch, thus lowering the final stretch.


Verifying point 1.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/8e699351-1d55-48e0-bd43-9ea1d898f1dc" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/1c2e9e19-12b1-4497-8ef5-c49f11e91ac6" />

Assumptions made in point 1 are thusly verified.



Verifying point 2.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/54242ba9-7d1a-447d-966e-da8a457d65b3" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/64eb3115-81cd-4b67-a791-e2d9b3f19465" />

Assumptions made in point 2 are thusly verified. However, I did not expect for the length of the rod to decrease.



Verifying point 3.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/e0d47348-382d-4cdc-a448-62459d7e4a8d" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/2b699f12-d7d5-4785-9a57-486939d24cf3" />

Assumptions made in point 3 are thusly proven false. My solids knowledge however is not sufficient to understand why this may be the case.

## [CAD file download](https://drive.google.com/file/d/1S985EJPT92NeRNLIvPmbMN9XGMjNrAUM/view?usp=sharing)
