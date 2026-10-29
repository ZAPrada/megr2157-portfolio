# A8 – Gears

## Objective

For this assignment, our main task was to design a single speed gearbox which was capable of outputting 1.25 in-lbf of torque and be able to spin the output at 1100 rpm. Additionally, the main part we would be designing was the housing for the gearbox as the dimensions of the shaft are mostly decided on, and the gears and bearings needed would be pulled directly from McMaster-Carr.

## Shaft Verification

To begin with, I needed to make sure that the shaft dimensions of the given gears were sufficient for the torque and rpm's required of the gearbox.

First, I noted down all of the knows of both the input and output shafts, as I would need information from both of them.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/44c65254-5726-4b27-a5c3-4015bbdb02b0" />



Then I listed all the unknowns of the input shaft that would be necessary to decide if the given shaft diameter of .125in was sufficient for the torque output required.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/c74d1aa4-bd1a-4add-b947-fd070e4af5ab" />




Then, roughly modeling what the FBD of the gear set would look like, I can get the idea that as one shaft receives torque, the other one will receive a different torque proportional to the torque of the first shaft. 

<img width="500" alt="image" src="https://github.com/user-attachments/assets/bd9af6a0-e45a-4991-aec3-64d643057ab6" />



Finally, I calculate based on formulas in the Machinery's Handbook and the in person lectures that with the given parameters, the diameter required to output the required torque is less than the actual diameter of the input shaft, as well as the stresses applied on the shaft from the required output are less than the maximum "safe" values mentioned in the Machinery's Handbook for a power transmitting shaft.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/9eb864c5-b134-4ee8-8001-b7e3ccd73515" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/05d9f64e-7d84-4035-b827-199f254c137e" />




Then, following a very similar process, I find that the output shaft similarly is well above the minimum shaft diameter and well below the maximum allowed stress for a short shaft.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/0f72d172-3a34-4cc0-9a84-eb7945ebd37f" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/2c5b796c-2e47-4bc5-ac4d-68e4ff221493" />



## Bearing thickness calculation

In order to select a journal bearing, I first needed to calculate a PV value which I could then compare against table 4 in the Machinery's Handbook to select a material. To calculate this, I chose the area to be half of the total shaft's outer surface area, as per the in class lecture, only the radial force of the gears would need to be accounted for, and as the radial force only comes from one side of the shaft, it at a maximum can only apply a force across half of the outer face of the shaft.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/43dc80eb-f766-4bf8-be15-9320809374dc" />


### Calculations for journal of input shaft 
<img width="500" alt="image" src="https://github.com/user-attachments/assets/1eb6152b-2a88-4b52-a072-d926083dd059" />

### Calculations for journal of output shaft
<img width="500" alt="image" src="https://github.com/user-attachments/assets/c57c610f-596e-4b0f-bfd0-34a35c4b16fc" />


With this PV value calculated, I then selected Porous bronze as my bearing material, as its properties were well above the maximum forces and surface velocity required of the output of the gearbox.
Using this, I then calculated the maximum deflection that the bearing will experience, and selected that to be the _minimum_ thickness that the bearings would need to be at.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/c595176c-e687-4a2f-9821-3acb737c12d4" />



As both of these minimum values of thickness are much less than any journal avaliable from McMasterr, I was then free to chose any thickness bearing I wanted without needed to be concerned with structural integrity.


## Sketch of 2 componant gearbox

I decided that my gearbox would be very simple, with 2 ends having "hooks" which will simply slide over small ledges and essentially lock the lid of the gearbox over the main body of the gearbox, with the input shaft coming in one end and the output shaft coming out of the other being used to restrain the lid in the perpendicular direction.


<img width="500" height="838" alt="image" src="https://github.com/user-attachments/assets/e376c06f-8579-4832-808c-6e6232050a61" />


## Gearbox CAD Model

I first began by creating the input and output shafts, which were modeled parametrically based off an external .txt file so that I would be able to easily change one variable and have it effect all of the design in the later assembly.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/704dfa35-fced-46c7-953e-460d1e9cfb6d" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/3f0c2b29-96a4-44cf-9744-4501daf2216a" />



### Input shaft 

<img width="500" alt="image" src="https://github.com/user-attachments/assets/be738c58-3e25-4252-9b62-a2908380599c" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/d970d19d-b37e-474a-bcf5-60ce024dec5a" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/476fdbb2-ad72-452c-816f-ebc8e1b0a158" />


### Output Shaft

<img width="500" alt="image" src="https://github.com/user-attachments/assets/9881238a-21fa-422b-93e3-d9a0d56df273" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/0b4968d0-d0d9-4db2-a0d7-d545a2d43a13" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/2dd96fe0-d551-4578-b8cb-d2cdcc0910aa" />


### Gears

I then created a new assembly file, in which I placed both gears required by the assignment, as well as mating them together so that they would behave as gears should.


Placing the input gear while mating it to the origin of the assembly

<img width="500"  alt="image" src="https://github.com/user-attachments/assets/2400f090-8c2f-4f85-b6c2-2671dbad142a" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/f7aeaf07-1700-4dbe-a86d-33c58757cf18" />



Placing the output gear while mating it to the other gear

<img width="500" alt="image" src="https://github.com/user-attachments/assets/595435a5-b4cc-4282-9473-68e7b509a40c" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/f63657a5-4430-4b56-a90d-1f807e80f652" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/84a07b12-56e6-4c47-a127-f2e6b093e73d" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/0f9a1287-803b-43b4-b183-e749863552aa" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/24d4fd8f-7775-4963-80f5-0f6ed53383a8" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/a57ab44d-3c5e-4bac-ba6a-80f2650618c4" />


#### Final Mated gearset

<img width="500" alt="image" src="https://github.com/user-attachments/assets/e6bd41b6-5f93-4f2c-bd85-719a8ab0feb6" />


### Shafts

I then opened the previously made shafts, and inserted them into the appropriate gears while making sure that they are flush to the opposite end of the gear.


Driving gear shaft

<img width="500" alt="image" src="https://github.com/user-attachments/assets/e098a2a1-410e-46f5-b449-f0578f63dde4" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/287637ab-7679-4f7a-99d4-c5fa7b312c53" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/d48795dc-13a3-46b4-87f4-24112db604d3" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/efd9aa89-e583-41e1-b7ef-8340ad2b39e0" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/68aee9f0-7c7c-42b8-817d-886cc21f7ff7" />



Driven gear shaft

<img width="500" alt="image" src="https://github.com/user-attachments/assets/b58e5031-a686-4125-b01d-f40d1d7ffef7" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/39768651-b17e-4116-b66c-6aae29fd169d" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/f729dc3c-1964-41fe-bb12-89eba44f00cb" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/345d5cb9-e92e-4dae-b4b0-bac2058fa49f" />


### Gearbox Design

After successfully inputting the shafts, I then went about designing the gearbox based off my sketch. I ended up needing to make a few adjustments to my variables file, as I was unable to reference them directly in the assembly. In designing this, I chose to define only one half of the box, and then simply mirror it, so that I could save on time by working with symmetry.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/59c9b745-b338-4c5c-a330-bc2dcf3b6d15" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/63d46e6a-34e7-414a-8d5f-335c85d994a5" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/af23245b-60a4-4b7c-b77f-b25a0eb2679c" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/c6c1c370-7951-4428-b64c-42da1d76f188" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/12b47c91-15a1-43f9-896a-b412ad3fb43a" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/dda67d94-61ee-420e-8b4c-548a9af1c3fe" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/74a430ce-6d9a-469e-a065-f8c208050b3d" />




I then extruded the sketch out to a point that fully encapsulated the gears and then some to ensure the gears would not crash into the gearbox. While also added the missing flanges on the 2 flatly extruded sides.


<img width="500" alt="image" src="https://github.com/user-attachments/assets/7315ad77-0cf3-47fc-a588-6ef9b7fe3ab7" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/17b43727-9ea6-4393-86ca-5982a643a1d6" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/cc114c06-0509-4b81-80d0-0db8291f0f35" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/0c327970-fad7-401e-9430-55f445a1163a" />



Then, I shelled out the extrusion so that it could be a box.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/ad47c621-a086-4d6f-a2e6-e793f392e265" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/1c921586-2f44-4169-ba8d-febd48025cca" />



Penultimately, I created the lid for the gearbox incorporating the hooks into the lid which would hold the box down, minimizing on parts needed for assembly.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/9ce97166-146f-4d3f-a085-c28250cde649" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/6afd7ffb-7288-4693-bd16-aefd07c664f2" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/0323755b-bf73-4dff-b8a5-200792716861" />


### Inputting journals and cleanup

I think in an extremely similar process to the gears, found journals which were an inch long and fit over top of my shafts from McMasterr, and inserted them into my assembly, changing the color of them so that they would be more distinct, and mating them properly to where they belonged.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/8b5d4e3a-edc1-43bb-b244-c5f560c005e0" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/83270ba7-6471-42dc-aaef-570f6ec0ee5f" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/673de7b6-019c-4027-b228-54a077e36069" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/776b7d27-f195-4484-a4df-ea335df5c1b4" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/9b42f83e-8c84-4a21-b22a-d495f2c48152" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/1a0d9a66-90e7-4bcf-bb73-00a5201e48f1" />


#### Cleanup

Lastly, I used an extrude cut to make a hole in the body of the gearbox and the lid exactly the same size as the journals, ensuring a good fit. Additionally, I shorted the input and output shafts as they were currently much too long for my liking.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/e56957da-12fd-481d-a44c-e727e68613de" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/ffab2e79-747f-4cc1-b399-036901354763" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/d42fcbfb-2f1a-4d9f-beb6-01eb6509de22" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/e3abf539-9ba7-4547-afb2-5d55962a7af2" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/a684eaa6-fa5a-4f38-8999-e264814e0c49" />



### Final gearbox

<img width="500" alt="image" src="https://github.com/user-attachments/assets/eab93202-bdbb-4f27-942c-adef85b4b4ac" />


## Lessons Learned

Perhaps the biggest lesson I learned from this assignment was that there was an option in SolidWorks to import designs directly from McMasterr into your assemblies. I was aware that there existed the option for Fusion, but only for certain paid tiers, while it seems as though the McMasterr addon for SolidWorks is free for anyone who owns a copy of SoildWorks. Apart from this, I am learning the hard way that I really need to look ahead at assignments and start them earlier, as I ended up having to sacrifice sleep for this assignment.

Total time spent on this assignment: 12 hours.


## Download CAD Files

[Click Here](https://drive.google.com/file/d/1HwRSZhDR1nObeg_bF3YeOZcLB-42rrsw/view?usp=sharing)


## 2157 Specific Section

<img width="978" height="752" alt="image" src="https://github.com/user-attachments/assets/089fefc9-02e1-474a-88a1-0701c675ca39" />

<img width="1066" height="824" alt="image" src="https://github.com/user-attachments/assets/4a2defc0-700f-4c2e-bbfd-8c28524d46b9" />

<img width="1094" height="843" alt="image" src="https://github.com/user-attachments/assets/933221e0-da51-4b7b-b155-72c3e2256ca8" />

<img width="1085" height="836" alt="image" src="https://github.com/user-attachments/assets/d2be3956-e260-48ce-8002-dd1664ae2be6" />

<img width="1048" height="807" alt="image" src="https://github.com/user-attachments/assets/969730ed-2be0-402a-9293-756a26f2ba31" />

<img width="1098" height="845" alt="image" src="https://github.com/user-attachments/assets/741e65e8-5aaa-4af4-992d-176fe7a39e83" />

<img width="1013" height="780" alt="image" src="https://github.com/user-attachments/assets/9b9e208c-d40a-4f8b-9d83-c12497e05316" />
