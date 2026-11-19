# A11 – Motor Selection (Ezra Bono & Zachary Prada)

## Objective


## 3DCad of Motor Mount Bracket

I first began by entering all of the previously calculated variables, and setting them to a file for easier manipulation later.
<img src="https://github.com/user-attachments/assets/81197622-6e78-403b-af7b-ccd20dab0d3c" />

I then create a square set to the motor's width, and extrude it out to the calculated thickness.

<img src="https://github.com/user-attachments/assets/14601c09-b036-486a-b5fb-89d9f9cf4a1e" />

<img  src="https://github.com/user-attachments/assets/2c83e78f-8961-4897-b004-31e635501050" />



I then set the space between the top of the bottom face and the top of this new rectangle on the side to be the height of the motor as to maximize travel.

<img src="https://github.com/user-attachments/assets/e08661c7-4d42-4bf2-9875-bed0f70c41f5" />

I then extrude this out as well giving it the same thickness as the calculated bottom face, as to ensure all parts of the bracket will perform within spec.

<img src="https://github.com/user-attachments/assets/b0908625-81e7-4775-9858-9d4c76343a9c" />

I then repeat this process for the mounting face. making it a square of the previously mentioned universal thickness.

<img src="https://github.com/user-attachments/assets/ee941c85-93ba-4d99-ab36-74893948733a" />

<img src="https://github.com/user-attachments/assets/e260f591-1edc-4707-a8a9-66e3d6f0e8b3" />


After completing the one side, I simply mirrored all features to save on time and to work with symmetry.

<img src="https://github.com/user-attachments/assets/91b10ef6-6a39-4f82-9c33-b6e02234d311" />


I then created a plot of dots on where the mounting holes for the motor are, and use SW's hole wizard to easily create 4 of the exact same hole.

<img src="https://github.com/user-attachments/assets/b0235887-dede-40df-afb1-f9af383b1074" />

<img alt="image" src="https://github.com/user-attachments/assets/365ece2a-1cd2-40e7-9bb6-42569792f302" />

Then I created the center hole, oversizing it to ensure the motor face does not experience any tolerance issues.

<img src="https://github.com/user-attachments/assets/5c781502-caf8-4e1f-a03b-6b114e1355c4" />

<img src="https://github.com/user-attachments/assets/5084df25-68a2-4f6f-b66e-66e8a64f7e05" />



I then repeat this process for the holes which mount the bracket to the frame.

<img src="https://github.com/user-attachments/assets/e64a25e8-98aa-4f44-9055-53fe781d0fb4" />

<img src="https://github.com/user-attachments/assets/7dfbfed9-8542-4b0d-be10-9c4da44493f5" />

<img alt="image" src="https://github.com/user-attachments/assets/db3ac22b-5e42-4eeb-b249-4f3358739abd" />


Finalized motor mount bracket.

<img src="https://github.com/user-attachments/assets/afe03659-a3bc-4090-b1d9-9ef25c2a998a" />


## Verifying frame strength (Zachary Prada)

To verify the chosen frame pieces would withstand the forces, I first choose a material in solidworks which had a similar yield strength to the material of the given frame, and then split the faces in order to better represent how the motor mounts would be acting on the upper frame.

<img src="https://github.com/user-attachments/assets/1a49ac5e-2b50-4462-a3a5-5dedd755abae" />

<img src="https://github.com/user-attachments/assets/76fc299c-ef12-44bc-9bc1-b2d64625b06a" />

<img src="https://github.com/user-attachments/assets/27fb71b6-d186-476d-9832-885dffa692fe" />

<img src="https://github.com/user-attachments/assets/0ea2e46b-d2dc-4328-8f2f-bcb3ebecaa0d" />


I then set the sides to be constrained rigidly, as that is how the real model would be put together, and took the full 2kN force and distributed it among the 4 contact points.

<img src="https://github.com/user-attachments/assets/a5804613-8c7d-4c2b-b67b-61fa7bf61405" />

<img src="https://github.com/user-attachments/assets/da55139d-7099-496c-8125-f30d96cee49a" />

Running the first test at SW's most course mesh setting, we can see that the frame is holding strong.

<img src="https://github.com/user-attachments/assets/83fcb365-0ff4-4932-86f6-116e014e0cb8" />

<img src="https://github.com/user-attachments/assets/7b2de121-27d3-4770-9304-5e829abdc0ed" />

<img alt="image" src="https://github.com/user-attachments/assets/47ccdadd-8b59-4bc1-aeb6-87db98db6d60" />

<img src="https://github.com/user-attachments/assets/13596b41-5320-4502-b393-917fd95a517a" />


Running the test again, we see that the finer mesh gives us different results, but the results converge to just below 10%, allowing us to conclude that the beam will be able to withstand the forces applied to it.

<img src="https://github.com/user-attachments/assets/0649e761-46ef-4039-8cc7-b74de06d31c7" />

<img src="https://github.com/user-attachments/assets/e10085e7-4186-4722-9425-2e89e22b9b5f" />

<img  src="https://github.com/user-attachments/assets/8be5f5b3-ff8d-4ad4-b204-4fce37a0c4d0" />

<img src="https://github.com/user-attachments/assets/2126f4c6-3f43-4380-a524-3fc168937f15" />

<img src="https://github.com/user-attachments/assets/62ca2e7a-4ec8-460b-b537-8f3489423682" />

<img src="https://github.com/user-attachments/assets/e388f187-3134-44a0-8455-027f23968e10" />

Then, testing the vertical frame arms, the lateral force was found by taking the force of the motor and dividing it by the distance it was from the arm, aproximating the lateral force that the vertical frames would see, while each then would see 1000N of compression.

Running 2 tests whose values converge to below 10%, we see that even in this test, the frames are able to withstand the rated loads.

Test 1 

<img src="https://github.com/user-attachments/assets/f4b38099-2a6a-4345-aecf-51efa78a7f01" />

<img src="https://github.com/user-attachments/assets/2a054b03-4e64-47c2-9d0a-69073ea5e774" />

<img src="https://github.com/user-attachments/assets/498df809-c4b1-4717-8f8a-5abe3c708c38" />

<img src="https://github.com/user-attachments/assets/b795c0e7-e50c-48a5-a975-010629150e77" />

<img src="https://github.com/user-attachments/assets/41cba829-8104-4cfa-a8da-4e08e8e7f275" />


Test 2

<img src="https://github.com/user-attachments/assets/b7b2c41f-6721-49fe-8490-a641083d2b9f" />

<img src="https://github.com/user-attachments/assets/bc84819b-614c-4f42-a0ea-b0f076fd1ef8" />

<img src="https://github.com/user-attachments/assets/43d87a5d-d2a4-4402-b959-b0a79df4dd3a" />

<img src="https://github.com/user-attachments/assets/82d9d55f-d021-45c2-a280-01fd08cd973a" />

<img src="https://github.com/user-attachments/assets/6cd92881-78b9-4b63-8c01-7e7a92832345" />


## 3D CAD of bearing support (Zachary Prada)

I first created a rectangle with the calculated dimensions, placing the mounting screw holes one of their own diameter away from the edge, as to ensure plenty of bezel in the material.

<img src="https://github.com/user-attachments/assets/e7b2106f-a491-4b81-b17c-9afaff9f6a20" />

I then extruded it out about 1.5x the selected bearing size, to find a middle ground between strength while still allowing the bearing to be full enclosed from below.

<img src="https://github.com/user-attachments/assets/077d15c4-98a4-4b96-a226-79f6ec95bdfb" />

Lastly, I took the given frame pieces and measured the distance from the center (where the screw would be) to one of the rails, and set the distance from the mounting screw holes to the bearing holder to be that measured distance.

<img src="https://github.com/user-attachments/assets/545baf78-acad-4977-9777-da5200a4d56b" />

Finalized bearing support

<img src="https://github.com/user-attachments/assets/b1c824bd-4f8d-4f85-a943-6a92ac2e0aa5" />


## Lessons Learned (Ezra Bono & Zachary Prada)

The biggest lesson learned from this assignment was that parts with many faces (such as the frame) take much longer to perform FEAs on. As we had to rush in order to finish the FEAs on time, but the computer took several times longer than our other FEAs on simpler geometry. In this, we began to really see the value of convergence tests, as it may not be the wisest move time-wise to simply go for the finest mesh setting and let the computer run for 10+ minutes.

Total time spent on this project (both team members summed): 22 hours.


## 2157 Specific Section (Zachary Prada)

<img src="https://github.com/user-attachments/assets/92fb845b-aea6-4d42-b36d-0a6034dbd025" />

<img src="https://github.com/user-attachments/assets/2e090355-9096-4d7a-a2d1-7286ed936011" />

<img src="https://github.com/user-attachments/assets/f917b258-d6ef-4f2f-b4eb-be3466e62715" />

<img alt="crosshead" src="https://github.com/user-attachments/assets/7e3e2422-de37-424c-95c5-a487b404dc48" />


