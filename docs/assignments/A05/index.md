# A5 – [Topic]

## Objective

For this assignment, I was tasked with designing a mount that would mount to a T solid T bracket (below), following certain design criteria such as rated load, maximum deflection, and fit, focusing primarily on ASME fit standards.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/aa0c457e-b524-400f-b011-dd79d0658c7b" />


## Analyze

To begin with, I first analyzed the design presented in appendix C.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/ff6a2cc2-9458-45ad-8058-048270f91a4b" />

Knowing that a load of 500 to 800 lbs was going to be placed on both ends of a strap that was to be draped over section A, I began by placing a distributed load all across the surface of A and then "tracing" the forces through the part.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/96517ff9-5025-4f6b-8186-31fbc2bab55d" />

In order to obtain these traced forces. I first let the strap be putting an evenly distributed force across the top of section A (which I would treat as a cantilever for the sake of analysis), which then would produce a reaction force that would translate into B, compressing it. I then assumed that that compression would then translate into a point force onto the center of C. C would then be treated as a simply supported beam, which I would then use to find what forces would translate into D. Assuming that the reaction forces in C become "distributed" through C as they pass through, they would then reach the face of D as an evenly distributed force pushing up on D. D would then be treated as a simply supported beam with the reaction forces from C pushing up on it. Finally, as D does not take up a large portion of the bottom surface of E, I assumed the reaction forces in D would act as a point force on the end of E.

Finally, to decide certain physical material properties, I chose ASTM A36 as my chosen material.

## Design

### Design for strength

To begin, I first assumed that the length of A would be the same as the width of the strap provided (0.75in), so that my even force distribution assumption would hold true. Using this and the formula for diameter of a round beam on page 263 of the Machinery's Handbook, I am able to find the diameter of section A.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/27c9d641-3747-46e2-8f9b-4a9bffb2ef85" />



Following this, I am able to use the standard stress formula to calculate the cross sectional area of section B. As area contains 2 values however, I set the width of section B to be equal to the diameter of section A so that everything would be nice and flush.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/a8313ce4-b857-4274-b9f2-87cd4087cf8f" />




Calculating section C however turned out to not be nearly as simple. As I fixed width for C based on the dimensions given in the initial instructions for the T bracket, I originally tried to optimize for volume by making height a function of length and analyzing it, however I could find no mathematical way to find an optimal value of height and breadth that would give me the smallest volume. 


<img width="500" alt="image" src="https://github.com/user-attachments/assets/0758ff4c-b971-44f1-b3f2-72baac8a501e" />
Width of section C would need to be at least _a_ + 2*_b_, thus 2.5in

<img width="500" alt="image" src="https://github.com/user-attachments/assets/42c04ae3-e77f-4c72-a3a9-fd05bea26af6" />
Failed optimization via graphical measurement (eyeballing a "middle" value, or the median slope).



Thus I set the breadth to be 2 times that of the thickness of section B.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/b14d2c85-c825-496e-aa68-084e8797bc02" />



Using this breadth value for the breadth of sections D and E, I was then easily find the width of section D by setting the height equal to _c_ from the initial T bracket dimensions.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/906e40d6-4b4f-4a80-9332-53d89359bacf" />


And find the height of section E by setting the width to _b_ from the initial T bracket, plus the width of section D.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/1db00dbb-60c2-4c3f-8a39-7c3bd23ddebf" />



### Designing for stiffness

Using the same rationality and assumptions used in designing for strength, designing for stiffness went by extremely quickly. All the unknowns and FBDs would stay the same, the only element that had changed in my calculations were the formulas used, pulled instead from page page 255.


First, I calculated the diameter of section A

<img width="500" alt="image" src="https://github.com/user-attachments/assets/7d736348-7b7d-499c-88d7-283de33c8dc4" />


Then applied the same axial compression assumption as previously done, setting the breadth of B equal to the diameter of A, and solving for B's thickness.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/919f10e8-e427-4806-b210-55e52a471743" />



Again, assuming that the reaction forces in B would produce a point force onto the center of C, which we assume to behave like a simply supported beam

<img width="1217" height="763" alt="image" src="https://github.com/user-attachments/assets/568ec83e-e733-47b9-8f3f-653fdc9559b1" />



I then unexpectedly ran into difficulties when calculating the width of section D. For whatever reason, the width of section D comes out to be 30 times that of the next highest value calculated. I attempted to analyze both that I had done the algebra for all the steps correctly, and analyzed the formula to see what could be changed in order to bring the width down to a reasonable size. However, all of these attempts ended in vain, and I was fairly confident I had done all the algebra and applied all the formula correctly, and realized I would have to change one value by a drastic amount in order to have a noticeable effect. As such I simply accepted that there was either an error I couldn't see in my calculations, or that there was a solids principal I simply was unaware of and/or applying improperly.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/9fd6d9b6-2280-496f-848d-3ea0e2ca11cd" />



Using this value like how I had previously done, I think was able to calculate the height of section E, finally completing both design's with their complete dimensions.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/bf396644-ca9d-49a2-a8c7-a313c3cdccca" />


## Design Drawings

Once my nominal dimentions were complete, I was able to turn my focus to making sure the parts I had designed met the fit criteria set up by the assignment. Based on the instructions given, section _a_ was an R7 class fit, section _b_ was an R3 class fit, and section C was a class R1 fit.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/0954bc92-61e4-464b-982b-f1c5a1e5da7a" />




Using the ASME fit standards table on page 654 and 655 of the Machinery's Handbook, I was able to then take my nominal dimensions and add the required tolerances to ensure a proper specified fit.\


#### Designed for Strength Drawing

<img width="500" alt="stress" src="https://github.com/user-attachments/assets/1a35550e-0d58-428a-807b-2a9c47b1ef63" />




### Designed for Stiffness Drawing


<img width="500" alt="displacement" src="https://github.com/user-attachments/assets/14ae3406-7eeb-4abc-85b8-fbabad4c4846" />




## Communicate

