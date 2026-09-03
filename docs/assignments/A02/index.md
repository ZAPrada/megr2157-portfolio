# A2 – Truss Stress Analysis

## Objective

For this assignment, I was tasked with designing a lightweight planar truss using A500 steel or equivalent material. During the designing of this truss I created a free body diagram (FBD) of the truss, calculated internal forces due to applied loads, and calculated the minimum cross sectional area to provide adequate strength for the material chosen. In addition to these calculations, I also modeled the truss in Solidworks so that I may run analysis on my design and evaluate if I did my calculations correctly.

## Analyze

As I unfortunately started this assignment late, I did not have much time for analysis. I mainly had to do light research into what sheer forces and stress/strain was as I have yet to take Solid Dynamic and am thus unfamiliar with the concepts. All of my subsequent analysis then was from a point of extreme ignorance and I believe I calculated many things incorrectly. Apart from this research on Solid Dynamics, I analyzed how I was to design this truss by seeing the design requirements, formulating the first thought that came into my head, and executing it immediately as I was short on time. No analysis was done on which frame type may be the best option, apart from the general knowledge of "triangles are strong" and building a truss that contains only triangles and hoping for the best. I did however go forward with the assumption that the truss would be horizontally symmetrical along a vertical axis via noticing that the dimensions given for the size of the truss were all neat clean easily divisible numbers.

## Decide

### Truss Calculations

I began by reading and understanding what my design restrictions and expected criteria were. I was to design a truss with 4 given points and expected to make it stable. When first analyzing the given points I noticed there were not enough to make a stable truss. Thus I added one in the center of the top (E) and added two members to connect from that new point to the existing points C and D. After this I went through using techniques used in Static Analysis, such as method of joints and method of sections, to find all the relevant forces at the supporting pins, and all the internal member forces.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/e885ffd0-9f9c-4159-8772-c55f70a3bfb6" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/4d129342-16b9-4b36-bb28-8d65243b4c11" />

After this I found that the largest internal force experiences in the truss is by members DE and CE, both of which experiences a load of 17024 Newtons.

<img width="800" alt="image" src="https://github.com/user-attachments/assets/28e475ce-d055-4ad7-ae6a-2e37fff62793" />


Using this information I was able to use the given safety factor of 3.5, the yield strength of the material I was to use (which in my case turned out to be ASTM A36 Steel as Solidworks did not have an option for A500 steel), and the stress formula to find the minimum required cross sectional area of 237mm^3, which I then took the square root of to get the sides lengths of the square cross sectional of my truss.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/e35798d1-45e1-4efb-a469-4d8e155ab5ec" />


Additionally, I then used the length of all of the members times the cross sectional area to find the volume, which I was then able to use to calculate both the total mass of the members of the truss and their weight using the mass density of 7850kg/mm^3 given via the material properties in Solidworks.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/f358eab8-04c4-487d-a0f1-6ec87a8ce2da" />


### Pin Calculations

After calculating all relevant information about the members of the truss, I then moved onto the pins which was a very similar process. I knew neither of the top 2 anchor pins would be facing the highest amount of force as I had calculated all forces acting on them and knew it to be less than my initial loads of 20kN. Thus I took an educated guess that the pins that would experience the highest load would be the ones directly acted upon by the 20kN force and did my calculations from there. 

<img width="500" alt="image" src="https://github.com/user-attachments/assets/467db03b-17e2-49b4-8192-c659bffc9247" />


To begin the calculations I first converted all the given units for the material of the pins from imperial to SI units, as the rest of my work had been in SI units and I wished to keep things consistent. I then followed the same process I went through with the main body of the truss, using the given yield strength, safety factor, and known force to calculate the minimum cross sectional area. However, this time I assumed that my cross sectional area would be a circle and calculated my mass and weight with this in mind.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/704d42e4-5bd8-4f76-8ead-8ac7cea146dd" />


### Truss CAD Modeling

After completing these calculations, I opened up solid works and began modeling. Firstly by drawing out the main outer shape of the truss, defining the majority of the shape with relationships due to the truss' symmetry and that many compounding dimensions can make the sketches messy.

<img width="400" alt="image" src="https://github.com/user-attachments/assets/e47c56aa-ab15-45c7-91cf-fc562d98ef2e" />

I then used the equations feature in Solidworks to define the side length I would be using constantly throughout the modeling, as there would be many dimensions which I would define that would use this same dimension, and using the equations feature would allow me to change them all at once in the future if I wished.

<img width="400" alt="image" src="https://github.com/user-attachments/assets/4bd67233-60fc-4c05-b938-a1e87d0af388" />

I then extruded the main body of the truss out using this "width" dimension as this dimension is one side of the square that is my cross sectional area.

<img width="400" alt="image" src="https://github.com/user-attachments/assets/28f2f52d-f372-4c3b-ba11-85ece26fa4c2" />

I then made a sketch, using many parallel and horizontal relationships, to define the inner void sections of the truss, using the mirror tool to take advantage of the symmetry and having less things to define manually.

<img width="400" alt="image" src="https://github.com/user-attachments/assets/338bee8f-24b6-49ba-9d47-7df1fce7850c" />

Finishing the main body of the truss, I used a sketch with defined points that I placed roughly in the center of where the pins would be, and Solidwork's hole wizard feature in combination to quickly place multiple holes for the pins. I decided to go with this method to make changing the hole sizes in the future much easier, as I would only need to change one variable instead of 5. Additionally, drawing the sketch allowed me to better specify where I wanted the holes, and then when using the hole wizard, allows the hole placements to automatically done, thus alleviating my workload. 
Again, using symmetry and the mirror tool to lighten number of hard definitions.

<img width="400" alt="image" src="https://github.com/user-attachments/assets/ecf59792-d4a4-4968-a92e-9a009d3d0f31" />

Using the radius calculated from the cross sectional area of the pins, multiplied by 2 to get the diameter, to size the holes.

<img width="400" alt="image" src="https://github.com/user-attachments/assets/dea0dad0-8fb6-42e9-baa6-b1c1eb7c7a16" />

I chose not to add extra material to compensate for the holes, believing that the cross sectional area with the safety factor would be sufficient in keeping rigidity. Additionally, after many tried and failed attempts, I could not figure out a way to accurately maintain the minimal cross sectional area without adding excess weight.

The finished truss.

<img width="400" alt="image" src="https://github.com/user-attachments/assets/ec3557b2-9598-4d51-9f09-2c9759e247a0" />

### Pin CAD modeling

The pins were in comparison, extremely straight forward. I merely set the length equal to that of one side of the cross sectional area of the main truss, and then extruded a circular sketch with the previously mentioned radius to complete my pins.

<img width="400" alt="image" src="https://github.com/user-attachments/assets/4dc20541-e6fd-460f-b62f-d6c2db349371" />
<img width="400" alt="image" src="https://github.com/user-attachments/assets/cf8d8002-caac-4b7a-9467-9a1a625a56ec" />

After Completing both the truss and pins, I then set about making an assembly of the two to test to make sure all of my mass and strength calculations were correct.

I began by importing the main truss into a new Solidworks assembly and fixing it in place so that I may have a "base" to work off of.

<img width="400" alt="image" src="https://github.com/user-attachments/assets/f274e270-d4f6-4a5a-ae58-bd12331e2fdf" />

Then I added 5 copies of the pin I created and used the Mate feature to easily place the pins exactly into the pin holes in the truss.

<img width="400" alt="image" src="https://github.com/user-attachments/assets/97bb8f23-954d-4089-99c7-a4ea2b31c1a4" />
<img width="400" alt="image" src="https://github.com/user-attachments/assets/f6aa6b95-aee2-49cd-bc04-22f80cd77a3a" />

The completed truss and pin setup.

<img width="400" alt="image" src="https://github.com/user-attachments/assets/2fe0f817-0895-462a-b18a-f32d00f1f15e" />

### Finished model analysis

Viewing the mass calculations done by Solidworks, and comparing them with my expected results, I came to the conclusion that my ignorance in the subject of Solid Mechanics caused me to commit huge errors in my calculations, calculating masses orders of magnitude greater than the part's real mass. Additionally, I am unsure of the final truss' structural strength, as I am extremely inexperienced in analysis using Solidworks and was not able to figure out how to properly test the truss' structural strength within the time frame of the assignment.

<img width="400" alt="image" src="https://github.com/user-attachments/assets/6ca9a7a3-f59f-41d3-9737-00e0aee3fc2d" />


## Communicate

I learned a lot completing this assignment, primarily in how little engineering math and theory I am actually knowledgeable in. As of the current moment, all design I have done has been very "off the top of the head," where I would use the intuition I have to construct things that may or may not work the first time. As it stand currently, I simply lack the skills to be able to properly, mathematically, create a functioning product. However, my ignorance shrank by an ever so slight amount in completing this assignment. I got to learn, vaguely, what stress and strain are, how they relate to forces and area, and how you can optimize for a certain outcome of the 4 using certain given criteria. Additionally, I have learned that projects such as this need much more attention to detail than I had previously thought, and that to be a proper engineer, one must set forth the right amount of time to be able to create an adequate product. All in all, though it may not be adequeate, the around 8 hours I spent on this assignment were extremely worthwhile.
