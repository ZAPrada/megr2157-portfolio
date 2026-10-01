# A6 – T Bracket CAD Drawing

## Objective

For this assignment, I was tasked with creating a CAD drawing of the bracket designed last week, which includes tolerances, and fit specifications for a parametrically designed 3D model.

## Analyze

To begin with, after reviewing my work from last week, I realized I made several mathematical errors. As such before creating any CAD model, I double checked all my formulas and made sure all of them were applied properly and were using the correct variables.

After reviewing all my math, I took note that for all features of the the bracket, designing for stress gave values which allowed for both sufficient stiffness and strength. Thus when designing the parametric model, I chose to use my equations solving for strength.

## 3D Model

I began by first imputing all my fixed variables which were consistent knowns during the initial hand designing phase.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/ec68f899-0c4e-4400-80fc-69e40b94ebcc" />


I then began in the same spot which I started the hand design, the diameter of feature A. With this and all other dependent dimensions, I elected to create the parametric equation within the definition of the dimension itself instead of first creating it in the global variable section. This was done simply to ensure the global variable section wouldn't become cluttered with a long list of variables that would be difficult to keep track of. Additionally, I gave each dependent dimension a given name so that I could easily figure out what dimension I am later referencing.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/9a2e2e1b-cafd-43c7-a467-0e5424ccfe3e" />




I then extruded the shaft, making sure to define it as a global variable.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/eff6bea6-8e98-424b-b5fa-b58b99a352fc" />




The sketch for section B was then created by using mostly relations, as I wanted the bottom sides of section B to be tangent with the shaft to save on material. I then set the arbitrary height between the top of the shaft and the bottom of section C to be enough that the strap provided could easily fit through.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/291fbcad-3369-4bb4-a167-bb7137693bf2" />




I then extruded section B in the opposite direction I extruded section A to ensure that A would stay the length that I had calculated it to be. And, as the formula for the thickness of section B derives one of its values from the diameter of section A, I made sure to reference said diameter in the definition for the dimension of section B.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/2daedf21-0c06-4f23-97f5-7d990615f73a" />




I then began on section C, in which I used a centerline relation to ensure the feature would always be centered with both section A and B. Again, applying the formula derived from last assignment but replacing all the variables with references from within the CAD model. The only exception being the 2.5in measurement which is hard coded in from the requirements of where the bracket needs to attach.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/76b1ff35-0234-4738-9802-86668aa75bd6" />

It was also here where I needed to create a new variable, which would be my calculated thickness for sections C through E.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/dce6fe37-4901-4b6f-9468-6b9ae71b837c" />




I then extruded section C out in the same direction as section A, starting from the back of section B, by the previously newly defined variable.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/d49e4676-65de-4136-aef2-1b67e99ed7d2" />




Then the same process was carried out for sections D and E, using and applying equations derived from last assignment and inputting into them variables derived from previous steps, and only hard coding in coefficients or specific design requirements.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/fe001f82-08c9-4357-85d6-d88fd30ea377" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/a94a765d-a480-4dd5-acf4-9489134993e7" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/d2a88d2f-1e3b-47a4-b745-cf1e7e7c4e72" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/ae225dc9-0122-4412-a560-70f90334e204" />




After completing one side of the bracket, I then used the mirror feature in solid works to "abuse" the fact that the bracket is symmetrical and save time for designing.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/4b9e8bf4-a851-4d45-884a-a369dfeec939" />




### Finished part

<img width="500" alt="image" src="https://github.com/user-attachments/assets/819e8c72-6327-4ede-b1b8-5333777b68ed" />


## Drawing

I first opened a new drawing, and then using SolidWorks' preset data blocks, selected the ANSI size A and filled out the the needed relevant information.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/7c9f60c2-8dd0-48ad-92e7-7961d5006c2a" />




I then put in a front and side view of the bracket with hidden lines, and an isometric view which had to be put at a smaller scale than the sheet scale as it didn't fit in otherwise.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/d03bd725-e76a-4acd-8aa7-965ace7f6750" />




Then finally, I add all of the dimensions, and include the tolerances for sections a, b and c based on a being an R7 class fit, section b being an R3 class fit, and section c being a class R1 fit.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/37709e66-f63b-4b44-86e0-264de27b7fb1" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/3266fea7-fcd1-470b-81a5-f80cd82a266c" />

### Finalized drawing

<img width="2200" height="1700" alt="stress" src="https://github.com/user-attachments/assets/fc2239d0-b157-4ec1-9a60-3dcc23443a42" />



## Reflection

The equation that had the most effect on this design was easily the thickness of section C. As the original equation which solves for the height of a simply supported beam included 2 unknowns, I had to set at least one variable, of which I chose the thickness. Originally this thickness had been set as the same as the thickness of section B plus the length of section A, which decreased the height to a personally reasonable level. However, when designing section D, as the thickness of section D is equal to that of section C, and the thickness of section D plays a major role in determining the width of section D, I ended up needed to decrease the thickness of section C all the way down to only 2 times the thickness of section B, otherwise section D would become incredibly wide and the part would resemble a bird instead of a mount. Thus I had to make the "sacrifice" of having section C be slightly tall so that D wouldn't spread out its wings.

One dimension which needed to be a tight tolerance was the height of the "slot" (aka section _c_), as this was stated by the instructions to be a critical feature which would be mating with the provided bracket, and needed as little play as possible. For section _c_ I merely chose the its tolerance based off of the design requirements provided that said that _c_ needed to have a fit "where accurate location and minimum play is desired."  And based off the readings from the Machinery's Handbook, this would be classified as a class R1 fit.
One dimension that _didn't_ require such tight tolerances though was section A, the shaft on which the strap would mount. I didn't believe this needed to be so precise seeing as how there would be plenty of clearance on all sides of the rod to slide the strap onto. Due to this clearance, and our safety factor, unless the diameter of the shaft is off by an extremely considerable amount, the part will see no additional stress if the part is smaller, or or clearance issues if the shaft is too big. Thus I simply left the dimension as unmarked which would then default back onto the tolerances marked in the data sheet.

In all this project took me around 7 hours to complete.

## Appendix

[CAD files download](https://github.com/user-attachments/files/32908615/stress.zip)

Image of full equations list

<img width="800" alt="image" src="https://github.com/user-attachments/assets/82a8019d-afe8-468a-8174-30d48c45225f" />



# 2157 Specifc section

### CAD Design

To begin, I started by copying over all of the variables from the earlier part of this assignment, only adding the elasticity modulus and the simplification for area.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/d1bfff52-b22d-48ad-a366-af2168473d7a" />




I then started the general shape of the using the slot tool

<img width="500" alt="image" src="https://github.com/user-attachments/assets/57048f81-a091-4fa2-8d90-a7739cc30e3d" />




I then set the diameter of the hole to be the exact same formula used to calculated the diameter of the shaft.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/68505b5c-8dd3-4464-828f-0cd2aba09cb2" />




Then, based off the minimum cross sectional area derived from the last assignment, I applied the formula derived for length (setting the thickness of the link to 0.25in) to be the length between the edge of the slotted circle, and the outer edge of the slot, to be no more than this distance. As well as making sure that the circle and the outer circle of the slot were cocentric so that they would always be this distance apart

<img width="500" alt="image" src="https://github.com/user-attachments/assets/12d598e3-5bfc-4401-9009-75f5aab3f7b0" />




Lastly, I applied the deformation formula, solving for length with a fixed 0.25in thickness, in order to get the total end to end length of the part. And mirrored the hole already created as to match the assignment design specifications.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/36f0e7d3-100f-431e-8e78-d4f0c36daaa8" />



Finished part extruded to 0.25in.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/85dc9379-33e6-4735-80c8-cd66c6c3d842" />


### Drawing of link

<img width="500" alt="link" src="https://github.com/user-attachments/assets/3bd49e21-6bb7-4c1c-a39d-eacdd96b24a3" />

### Reflection

When preforming tolerancing between 2 separate parts, I was strangely surprised how often I had to swap between the 2 in order to get the dimensioning right. I would have assumed that once you applied the tolerances to one part you would be done, but instead I needed to constantly reference both parts to ensure that one would actually fit in the other, and that they wouldn't crash into each other.

I believe that there is a linear relationship between tightness of tolerance and "professionalism." If a part needs to be designed within 0.0001in, that part most likely is being used in an extremely sensitive or high performance application, where anything short of actual perfection is unacceptable. Additionally, if a part is dimension to a precise enough, that would give the designer/company working on the part seem more "prestigious," effectively waving a sign saying "look at us, we're able to manufacturer something to this high of a standard of quality." While low tolerances and dimension conveys the exact opposite.

[Link files](https://github.com/user-attachments/files/32910064/link.zip)



