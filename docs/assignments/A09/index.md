# A9 – Pulleys

## Objective

For this assignment, we were tasked with selecting a suitable band which would withstand 4-6lbs of belt tension for a pulley system in which 2 3in diameter pulleys were 6in apart (shown below) and spinning at 1000-2000rpm, and then fitting a shaft and bearing within the pulleys so that they both may be mounted to a bracket. Primarily, this assignment tested our skills and knowledge in how pulleys operate when moving, as well as how to find minimum spec values.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/c7522082-3739-4943-a5bc-d210884080e9" />


## Pulley band selection

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


## Minimum Shaft Diameter Calculator

Part of the assignment was finding a shaft made of 1030 hardened steel which could be inserted in the pulleys and withstand the torque produced by pulley's movement and translate the power accordingly. To do this I first began again by listing all my known and unkowns, while drawing an FBD of only one pulley again to simplify the math. Most of my values were either previouslly derived, given in the assignment instructions, or derived from Matweb when it came to material properties.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/7dde2c5e-c0d1-4adf-89d1-21dafe741f88" />




I then converted the RPM to rads/sec, though I couldn't figure out how to originally solve this symbolically, I then decided to work out the conversion using ratios and multiplication as it was the only way I could wrap my head around the conversion. 

<img width="500" alt="image" src="https://github.com/user-attachments/assets/60f5e8d3-a95b-4bac-aabc-847916a9b5f9" />




Then, using the formulas given in class for power and torque, I solve for the aforementioned variables which would be essential to later calculations.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/75807684-f773-4aa9-91dc-f7e1cb673d1d" />





Finally, I calculated the torsional shear using the formula found in the Machinery's Handbook to calculate the minimum diameter needed by the shaft to withstand the calculated torque load.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/1d01e086-7918-419c-84bc-3ca5bba005c9" />




Using this, I found the minimum diameter of the shafts for the pulleys to be 0.142in.


## Selecting appropriate bushing material


The final part of this assignment was to select an appropriate bushing material that could withstand the surface speed and pressure applied via the pulleys. To do this I first listed all of my u
