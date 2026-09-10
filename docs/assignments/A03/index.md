# A3 – Parametric Design Optimizing for Strength

## Objective

For this assignment, I was tasked with designing a cantilever bar with a circular cross section that, when in axial tension, would not stretch (deflect axially) more than 0.009in. The bar had to be made out of aluminum and had to withstand an axial tension load between 300 and 500 lbs. The main point of this assignment was to design this bar within CAD using parametric values. Essentially, only imputing a few variables, and then setting up equations with those variables, and then driving the dimensions of our bar based off of those materials. After our bar was designed, we were to conduct a Free Element Analysis using CAD to determine if, based off of our calculations, we had designed the bar correctly. 

## Hand Calculations

To begin with I needed to understand how the bar was expected to be loaded and setup, and after some time reading through the assignment instructions, I had come to the conclusion that it was to be a cantilever pulled along its axis by some force.

<img width="500" alt="FBD of bar" src="https://github.com/user-attachments/assets/03a3bc5b-eab0-4192-a1b3-b9d5f9c80f51" />

After noting how the bar was to be setup, I then went about figuring out the math which I would use to design the bar. As per the instructions, I went with direct tension elongation equation found in our Machinery's Handbook. This equation relates axial stretching (e) to force (F), length of the bar (L), cross sectional area of the bar (A), and the modulus of elasticity of the material the bar is made out of (E).

<img width="500" alt="image" src="https://github.com/user-attachments/assets/4c0b1ae8-924e-47ce-b2a5-31e8f6a275b1" />

After picking this equation, I then went about noting which values I did and did not know. 

Firstly, my knowns: I was given maximum axial deflection from the assignment instructions (0.009in), thus I set my value for e to 0.009 as when I went to solve for an unknown, it would give me the minimum value for that unknown which would meet the requirement of not stretching more than 0.009in. I then set my applied force to be the maximum given by the assignment, 500lbs, to again, let my unknowns grow to the largest they could be to ensure my final bar would be able to withstand the maximum load it may see. For my modulus of elasticity, I turned to SolidWorks to give me that value so that way my hand calculations would be accurate to my FEA. Picking **3.0205 (EN-AW 1200)** aluminum (99.5% pure aluminum) as my material in SolidWorks gives me an E of 10152641.64 psi. 

SolidWorks aluminium

<img width="500" alt="image" src="https://github.com/user-attachments/assets/d52074d7-3e2a-471e-827f-e430b4a7517a" />

As for my unknowns: I had the length of the rod (L) and its cross sectional area (A). As I had 2 unknown and only 1 equation, I wouldn't be able to create mathematically perfect bar given the specifications, as such I was going to have to solve for one variable and then choose a value for the other variable. After doing the algebra and solving for both variables, I decided on letting the length be the function of the other variables, and picking a value for A as the equation when solved for length was much more simple and neat.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/eea06642-afa2-4a9f-a92e-d1e4c81c8694" />

After getting my hand calculations and algebra set in order, I was ready to move onto the CAD phase of the design.


## Parametric Design in SolidWorks




## Communicate

