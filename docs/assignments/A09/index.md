# A9 – Pulleys

## Objective

For this assignment, we were tasked with selecting a suitable band which would withstand 4-6lbs of belt tension for a pulley system in which 2 3in diameter pulleys were 6in apart (shown below) and spinning at 1000-2000rpm, and then fitting a shaft and bearing within the pulleys so that they both may be mounted to a bracket. Primarily, this assignment tested our skills and knowledge in how pulleys operate when moving, as well as how to find minimum spec values.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/c7522082-3739-4943-a5bc-d210884080e9" />


## Pulley Band Selection

I first began simply by drawing a FBD of only one of the pulleys, taking advantage of the symmetry of the pulley design to simplify my hand calculations, as all of my calulcations could simply be done on one pulley and then transferred to the other. After drawing the FBD, I went about listing every known and unkown I could possibly have, though at this stage I was still a little blind and was unsure what exactly I would need, as such my unknowns contain some which I never end up calculating until much later.

I chose the maximum values given by the assignment as to design a pulley system that could easily handle all of the rated load cases.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/0178a59c-9f12-4dd5-bdbe-dd9a85b92db3" />




Then, I went about trying to understand exactly how I could go about solving for F1 and F2, eventually landing on building a system of equations based on the pully when the belt is not spinning, and the friction along the pulley in motion, to get F1 and F2 while the pulley is in motion.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/3fcd805c-40f7-42b4-a024-5174aa0c6ce4" />



After having a value for F1 and F2, I could then solve for the stress in the belt, assuming simple tension to simplify the math, and choosing F1 to be my force as It would be the greatest of the 2 and thus produce the greatest minimum area.


<img width="500" alt="image" src="https://github.com/user-attachments/assets/877a572c-d6af-4dcc-84d4-b78a2d65c84f" />




Using these derived equations, I can then numerically solve for the minimum diameter, specifically choosing the diameter as my final result as all of the belts sold by McMaster are specified in their cross sectional diameter.


<img width="500" alt="image" src="https://github.com/user-attachments/assets/523cdc1b-a905-4a86-8fee-c82b37a37d99" />



Now having one half of the belt specification, the only specification I was missing was the outside diameter, or the total length of the band. This was found simply by taking one half of the circumfrence of the pulleys as well as the distance between the pulleys, all multiplied by 2.


<img width="500" alt="image" src="https://github.com/user-attachments/assets/e2cc4fe1-4466-4eff-a25c-9ff020464a4d" />




Now with a minimum diameter of .29in and a maximum length (maximum as a band any larger would be too loose and not fit on the pulleys) of 21.42. I simply needed to find the round belts on the McMaster website and filter for belts which fit within my calculated specifications. In this case part #3044K608 with a cross sectional diameter of 3/8" and a outer circumference of 21 1/4".

<img width="500" alt="image" src="https://github.com/user-attachments/assets/10e53d10-bbd6-4eb4-8cc4-4e92d021c199" />


## Minimum Shaft Diameter Calculation

Part of the assignment was finding a shaft made of 1030 hardened steel which could be inserted in the pulleys and withstand the torque produced by pulley's movement and translate the power accordingly. To do this I first began again by listing all my known and unkowns, while drawing an FBD of only one pulley again to simplify the math. Most of my values were either previouslly derived, given in the assignment instructions, or derived from Matweb when it came to material properties.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/7dde2c5e-c0d1-4adf-89d1-21dafe741f88" />




I then converted the RPM to rads/sec, though I couldn't figure out how to originally solve this symbolically, I then decided to work out the conversion using ratios and multiplication as it was the only way I could wrap my head around the conversion. 

<img width="500" alt="image" src="https://github.com/user-attachments/assets/60f5e8d3-a95b-4bac-aabc-847916a9b5f9" />




Then, using the formulas given in class for power and torque, I solve for the aforementioned variables which would be essential to later calculations.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/75807684-f773-4aa9-91dc-f7e1cb673d1d" />





Finally, I calculated the torsional shear using the formula found in the Machinery's Handbook to calculate the minimum diameter needed by the shaft to withstand the calculated torque load.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/1d01e086-7918-419c-84bc-3ca5bba005c9" />




Using this, I found the minimum diameter of the shafts for the pulleys to be 0.142in.


## Selecting Appropriate Bushing Material


The penultimate part of this assignment was to select an appropriate bushing material that could withstand the surface speed and pressure applied via the pulleys. To do this I first listed all of my knowns and unknowns, and then drew an FDB of the pulley. I assumed the only force acting on the bearing would be that of the force produced by the 2 sides of the bands stretched to 6lbs along the entire surface of the bearing. Though this may be unrealistic, I chose it as to compensate for any additional stresses the bearing may encounter in the real world that I may not have accounted for. Additionally, I assumed the length of the bearing to be only that of the band's diameter, as this would perform a similar compensation as previously stated.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/45ce8116-cab3-4ee0-9d2a-35a784a4fa73" />




Finally, I could solve for my PV value.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/af08f077-14ae-4333-99f6-27c5326aaf9c" />




Then, referencing Table 4 for sintered metal or non metallic journal bearings found in the Machinery's Handbook, I found that Acetal would fit perfectly within my calculated minimum specifications.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/94dc0e07-2505-432d-aa4d-67b094e2212a" />


## Bracket Design

The final part of the assignment was to design a frame which would support the pulley system. I chose to imagine the frame as a simple beam in tension from the spring which would be applying tension to the band. Additionally, as it was only meant to be a frame, I chose to have the breadth of the beam be only half of the pulleys diameter, as the frame does not need to fully encapsulate the pulleys. Then, the holes in the bracket are the exact size as the calculated value for the pulley's shafts. Then with all these measurements decided via engineering judgement, I went about calculating a minimum thickness value using a safety factor of 3 and the previously researched yield strength of 1030 hardened steel, which I found to be .3 thousands of an inch. As this is smaller than even aluminum foil, I simply chose to set the thickness arbitrarily at 0.125in to give the frame proper rigidity, which still maintaining above minimum thickness.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/95d702a9-1c3c-47c2-a75e-b6f46be0f509" />



## Reflection

This assignment was initially a little scary as I have yet to take Dynamics, and worried that I would be completely lost when things such as the band and pulley began to move. However, given the lecture and Machinery's Handbook, I found that even if I don't have formal training in a subject, I am able to make by and still build a reasonable product that I believe would survive in the real world simply by overbuilding it a little.

In all, this assignment took about 7 hours to complete.



