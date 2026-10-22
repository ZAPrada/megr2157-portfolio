# A7 – Bracket FEA Analysis

## Objective

The goal of this assignment was to improve the previously designed strap bracket by conducting multiple rounds of Finite Element Analysis (FEA), through an "outer" design loop where design changes are made based on FEA results, and an "inner" validation loop where results of the FEA are validated. Specifically, this assignment asked to optimize for weight and strength within the outer loop, while having the inner loop of repeated FEA analysis be done until either the results converge within 7%, or 3 FEA studies are completed.

## Initial Factor Selection

As I had previously chosen ASTM A36 Steel as my material in my initial hand calculation, I had to keep with the steel in order to ensure my hand calculations could be verified by the FEA analysis. Additionally, I had set a personal goal that the minimum safety factor had to be 3. That is to say, when conducting my FEA and making design changes, I would not be worried too much about deflection distance, and instead would focus on designing purely for strength.

## Initial Design and FEA Setup

Taking the unchanged bracket from the previous assignment, I wanted to see if my initial hand calculations gave sufficient geomatry to allow for my minimum 3 safety factor, all while keeping a low weight. I was unsure that this would be possible due to the large "wings" that the bracket had, however I wanted to try anyways.

After taking the previously designed bracket, I first split the face of the section the strap would rest on into an upper and lower face, so that I could later more accurately apply the force on the bracket.


<img width="500" alt="image" src="https://github.com/user-attachments/assets/98ed8a89-ec8d-45ac-9963-ee7546753eff" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/adb4d32d-bb0e-44f3-a903-6cb127bf5bc7" />



Then, after creating a new study in SolidWorks, I set the faces that would touch the supporting feature mentioned in A5 to be solid fixtures, simulating the bracket being attached to the fixture.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/e6c5d82b-54a9-429d-80e9-7cb4b7d482fd" />



Then, as I had done all my hand calculations with 800lbs of force acting on the support beam, I added a distributed mass of 800lbs along the top half of the cylindrical face. Caveat with this method however is that I needed to define gravity in order for the distributed mass to behave properly. 

<img width="500" alt="image" src="https://github.com/user-attachments/assets/301a1c9b-faaa-484d-908b-f42b7780a64d" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/2d09c13b-c3c1-4113-a6e0-c5ac17437bd2" />



While I could have simply added an 800lbs force along the face, I wanted to take the mass of the body into account as I believed that the bracket would become sufficiently heavy enough for mass to play a significant role. Thus, with using distributed mass and defining gravity within the FEA, I get a more realistic expectation of the behavior I'd expect to see in real life



After this initial study setup was done, I could move on to performing the FEA itself on the initial design.

First, the mass of this initial design was 7.20 pounds.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/4d4bbe47-2f22-427c-9484-220bb738bbde" />



Then, I selected the most course mesh setting SolidWorks allowed, to allow for the shortest compute time. This gave me an element count of 1383.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/d1772120-17e0-47b4-8bab-7b10bf8baf6e" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/c890a000-e060-48b9-923a-9627992dc409" />




Then I ran the simulation and took note that while my displacement was acceptable, the safety factor in the section that connection the lower shaft to the rest of the bracket was below 1, meaning the bracket would have failed with the 800lbs load applied.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/01293571-927c-4030-a262-ffca707e4a99" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/10bf8152-8af4-4f5d-9e42-2b803632493e" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/bcc158a8-9961-4f25-9ec1-54d51bc4cb90" />




To verify the results however, I ran the simulation again, this time however using a finer mesh, which gave an element count of 10264

<img width="500" alt="image" src="https://github.com/user-attachments/assets/f7b45827-d0df-461a-9de9-429810e9307b" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/2fe175f1-e0f4-40e5-9cf4-322e27565222" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/c2d365ff-36ae-41b7-a2fc-f86d83cb0b46" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/9e2d2bd3-2234-49c7-a6a2-052e5a72c550" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/a4c1409d-290a-4a9b-9bbb-4bd18cc7fba1" />




Comparing the 2 results, we can see that there is more than a 7% difference between the 2 simulations, as such we will need to run the simulation for a third and final time.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/0fb9cb00-3206-47ca-9357-7a73c95e4de4" />




Running the simulation for the last time with the finest mesh size available, which gives an element count of 61650.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/86cf8985-5a2c-4ffa-b206-cad92f59bf27" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/717450e6-3999-4ac2-a788-961dc5b7a71f" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/98763ab4-1cf9-49c7-844c-0b2c2940ed4e" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/d8bb7aa7-c2f9-470d-b264-eb1961dd162b" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/00d05772-ca7e-4364-b153-394886be863b" />




Comparing these results with the previous mid-course test, we can see that they both don't converge to within 7%, and that our safety factor is below 0. Additionally, we can see that the finer the mesh we make for the FEA, the higher our stress becomes.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/555510ee-2d19-4f3a-8f87-14cace32669b" />


As the part was breaking and not meeting our factor of safety, revisions would need to be made to increase its strength.

## Design 2

I chose to focus all of my changes to around the section that connects the cylinder shaft to the main body, as that was the section with the highest stress by far, with every other section having a safety factor well above 3.

I first began by simply making the section thicker, specifically by a factor of 2.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/7291ce7a-38b4-462b-ad9d-fe8f9d276fa9" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/1a308a32-c3f5-4900-b145-894405dc734b" />





Then, I believed that the 800lbs was acting on the section much like a lever, as such I chose to decrease the gap between the cylinder and the main body by half, so that the 800lbs would have less leverage and hopefully produce less stress on the section.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/85f6aef6-ce61-4920-9760-1c3e66afe411" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/310dd8f4-3cae-467d-b1d7-1fe6676da727" />





This had the unintended consequence of elongating the "wings" of the bracket, however as they were not breaking, I chose to ignore that and optimize for weight later on, and to only focus and hone in on the minimum strength required.


<img width="500" alt="image" src="https://github.com/user-attachments/assets/1c09f14f-6868-4c74-8dc1-8189c0fb0307" />





First, checking the mass, we can see that this new design weighs 23.88 lbs.

And again, going through the exact same process as the initial design. I choose the most course mesh type, and then test for convergence.


#### Course mesh:
<img width="500" alt="image" src="https://github.com/user-attachments/assets/37720aee-a6e0-4586-a73e-e601e0cfb624" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/fd2aea4d-2580-4ae5-942e-ff9a8806609d" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/5bdbd2bf-3bf4-454a-8762-88ef5bcd2dd0" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/f089f731-b855-4a18-9ae3-c94ba2f7e34f" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/ef56a3a0-5b64-429f-84f0-ec5dd29a70a3" />







#### Mid-course mesh:
<img width="500" alt="image" src="https://github.com/user-attachments/assets/65e71c6d-5627-4ee9-a1ce-cf46c2aa244c" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/54b41cf0-3b74-4adf-b833-428d1e6aa60a" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/1a75d0b4-aa89-4db9-b737-9a84b5f4d931" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/80f12dbe-956c-4e31-964b-9d9b24614845" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/5f9d5e7e-7e28-41ea-ab3a-81459ef95993" />



Analyzing the results we see again that the results do not converge to <7%, as such we much run the final FEA for this design.

<img width="1456" height="170" alt="image" src="https://github.com/user-attachments/assets/bafa8b53-dc6f-427b-989a-e2e18643a2d6" />




#### Fine mesh
<img width="500" alt="image" src="https://github.com/user-attachments/assets/2bbf99c5-fff4-44d2-ab37-54d88e201d4e" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/4e5a020c-a910-434a-a9e1-28819eaaefce" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/d88d66cb-768e-4549-a481-4eda9a7124ba" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/98212801-faa1-40d1-b561-36724d60920a" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/b612cf95-4135-4a87-8d34-6313dece6a0b" />




Comparing the results of this test vs the last one, we see that while the results do not converge, the safety factor trends downward. Additionally, even though the safety factor trends downwards, even the highest safety factor is still less than 3, as such we will need to revise the design again.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/c8241191-377d-46f1-a4ce-c36244664b0b" />

## Design 3

As the stress again was consistantly consentrated in the section holding the cylinder and the main body together, I elected to modify only that section once again. However, as my gap was already very small, maybe even small enough to where a thicker strap would not fit. I chose to simply increase the thickness of the part to increase its strength. This time by a factor of 5 instead of merely 2.


<img width="500" alt="image" src="https://github.com/user-attachments/assets/dc3660b3-2314-4bfc-9065-82dc3bc86a4a" />





Again, this caused the "wings" to expand dramatically, and caused the mass to shoot up to 128.73 lbs, which will need to be addressed later as this is no longer considered a light weight part.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/0313aa83-e5ae-45a8-9dd9-dddbdfd1fd69" />




As before: I run a simulation using the same constraints and loads as before, only having changed the design and the mesh size.

#### Course mesh
<img width="500" alt="image" src="https://github.com/user-attachments/assets/115d0b88-e2f3-416e-a4d9-5d9678ea5378" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/a53084a8-c928-44ad-8577-11555bb5aefd" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/11ae985e-3744-4b6b-81e7-375faddb9445" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/8c1fda71-912d-4cf5-a8a0-14a1aa52edb6" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/7d56fd22-64db-4390-8637-293e19573420" />


#### Mid-course mesh
<img width="500" alt="image" src="https://github.com/user-attachments/assets/d0ff7d70-3d9a-4d47-aec3-435955e0e806" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/e3c11985-58c4-413c-aa15-cef4393420a7" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/e7dc84d1-6e3f-4ba9-8f1e-033d42e66a8c" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/7ba5e5d4-1819-4e63-9237-6105768399d7" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/5d28b70c-1d75-4cc6-a55b-449062c49c9b" />



Reviewing the results, we see that the values converged below 7%, and that our safety factor is above 3. Meaning that our part is sufficient in terms of strength. However, a bracket weighing as much as a teenager is extremely impractical, and will need to be lightened.


## Design 4

As the section connecting the cylinder and the main body was still where the highest amount of stress was being concentrated. I elected to leave that section alone and focus primarily on the long and thick wings, shortening them by a factor of 15, and halving the thickness, as the FEA showed me that (apart from deflection) the wings were extremely strong and stable, and most definitely could have some material removed while still staying sufficiently strong.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/adee18b1-a54d-4209-b2db-0c626071a66f" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/6e1f961a-2500-48db-898b-3aafbe526de1" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/824e5939-8a42-4c14-a230-c753fac6cb4d" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/ce3a73b4-ea43-4c35-ac46-cd3baab1365c" />





Evaluating the part now, we see that it's mass has dropped to a much more acceptable value of 2.61lbs, perfectly light enough for anyone to carry. Thought I staved off from making the whole body any thinner, as that would cause the weakest section to become even weaker.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/23c10478-495f-4d71-8877-247932dbc951" />



I then ran the same simulations using the same parameter as the start.

#### Course mesh
<img width="500" alt="image" src="https://github.com/user-attachments/assets/a4d27f0e-aeba-48cc-a793-15f2f15a2acf" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/886f892d-81f2-447b-b0ff-1a281241b70d" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/587b67fc-7f78-48d4-840e-473f4e9f29c2" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/b1a04e9e-4ac1-4c0c-9cf9-d08d4dc96c7c" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/5dfec903-26cd-4dbe-9d42-95ac06bf377a" />

#### Mid-course mesh
<img width="500" alt="image" src="https://github.com/user-attachments/assets/ced308c3-8e8c-4c2b-9303-99cf9da0ffe3" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/b7a6c3fc-c78f-4a26-9aed-efa4f26f782a" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/138eaa18-4c8a-40bf-b049-008c26ad5ad6" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/1a6f6882-9e01-41db-b372-6647122206cb" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/aaf1019d-b386-4986-ac1b-b4412d7a16ee" />


Analyzing the results, we see again that the results do not converge, but still trend downwards. As such a third test is needed. Though interesting to know, our safety factor went _up_ despite keeping that section of the bracket equal

<img width="500" alt="image" src="https://github.com/user-attachments/assets/8bd0b8d1-380c-40f3-9e1a-2b02fc93db58" />




#### Fine Mesh

<img width="500" alt="image" src="https://github.com/user-attachments/assets/d0c2efed-4f4a-4955-a951-6bca74c7a60b" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/f0534d19-dfc4-45a3-be33-d235f2677d25" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/98e41ff1-7a15-4489-9677-db6f3b9faa7f" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/4e3cd2ef-05ae-4ef4-b775-dbf0596cdf02" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/120a475b-9ba8-4ccb-8c23-5c297ce3c1d2" />


#### Analysis
<img width="1456" height="370" alt="image" src="https://github.com/user-attachments/assets/0303adb5-9f6f-4d7a-902b-91355ddbf1b7" />




Despite seeing that our values do not converge to below 7%, we can see that even with the most fine mesh (aka most realistic mesh) that we have a safety factor above 3, which finally meets our goal, as we can make too many more sacrifices to the part without compromising strength.


## Reflection

While I didn't learn a whole lot from this lesson, and when I test parts I have made or 3d printed, I usually try to measure the test components til failure after having physically made them, as I believe that will give me the best data possible for how to improve the design. However, I learned many things in this assignment about how to do that real life testing, but specifically within SolidWorks' FEA simulation system. This definitely will help me later one save both time and money on materials as I will no longer need to constantly build physical prototypes to test. Additionally, I much enjoyed how you could see exactly where the max stress and or deflection occurred, so you can much more easily pinpoint places that would need reinforcement. I will definitely continue using this tool later on in my engineering career, as I firmly believe that it will save me an immeasurable amount of both time and money, especially as you typically do not need an extremely powerful machine to run these simulations unless they are extremely complicated. 

Total time spent on this assignment: 10 hours

# 2157 Specific Section

Again, I have chosen a ASTM A36 steel, and a minimum SF of 3.0 as my design criteria.

### Setting up Analysis

Fixing one hole while putting a force of 800lbs on one half of the inside face of the other to best simulate the link being between the 800lbs force and the bracket.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/64e2e6c2-612f-4c91-a66a-5b58bc86b745" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/c1a34d58-6d32-4758-bc85-2cad8de53e81" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/c4915b2d-fbcc-47ed-ba28-a6d11cab3de2" />


## Design 1

Mass of 1.67lbs

<img width="500" alt="image" src="https://github.com/user-attachments/assets/af8a614d-e15b-402c-8bc0-d84f426b53e5" />


#### Course mesh FEA

<img width="500" alt="image" src="https://github.com/user-attachments/assets/862baa80-b100-4b28-a4f1-855b85762522" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/e93674d7-e447-4ba7-a69b-d9f7f817498f" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/12c4f3b2-a76a-44af-8b4f-b70a6aa279f8" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/24ffd14b-869b-4506-996d-925a8a5b4ea6" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/95fba747-9f5b-49f1-903c-2ee2f3d39f86" />


#### Fine-course mesh

<img width="500" alt="image" src="https://github.com/user-attachments/assets/5bedffc2-4d89-411e-abfc-173ba2a40828" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/4df1f457-1390-4d85-aac8-af7f52620e59" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/60f86df4-9aea-4f12-a2f0-f89b32c367ed" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/379b8ee2-f323-4c35-8aeb-eadfe821d211" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/74bd5984-3cde-4189-9fb7-0458dc9ea1d8" />





Results do not converge to <7%, therefor must produce third FEA.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/699b87a2-3245-49f4-b49a-58ff25f89ca4" />


#### Fine Mesh

<img width="500" alt="image" src="https://github.com/user-attachments/assets/d6017051-97e1-4717-8ee1-dc0210d0f305" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/d89a037a-5184-4361-80c4-80659fb04bf3" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/3f883764-06d3-427b-bbc8-e8a9112d22f5" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/5e500e22-8646-496e-a28b-003e53a20e8e" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/62d99b88-0f48-481f-a419-ec9531704fcf" />


Based off of these FEAs, length can be shortened, but link will need to be make thicker.

## Design 2

Length of link is divided in half, space between outer edge and holes increased by 1.5 times.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/d0df5941-8b60-4a1c-ba1a-8702490e96ad" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/2934f452-21d5-488d-b9d4-80c3bc0a69e7" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/1b3f23fb-2160-46c1-98c0-3e6686ff0ba3" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/f835ee0f-6306-409b-b516-37e697969fc3" />





Mass is now 0.96lbs

<img width="500" alt="image" src="https://github.com/user-attachments/assets/ba13f75a-77ad-4408-88e1-e60da9c383e5" />


#### Course mesh
<img width="500" alt="image" src="https://github.com/user-attachments/assets/d6e31df6-c42c-499a-92b6-dc8dab100cd3" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/6a4a693d-7148-43e9-86b4-ba5f29cb41da" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/303e4efe-b08c-4aad-b452-2b49601a1b23" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/fd921229-f687-4b6d-a569-0df2f88aa839" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/193c4883-1130-4866-a3e9-4cabaf7df081" />


#### Fine-course mesh
<img width="500" alt="image" src="https://github.com/user-attachments/assets/a51f796b-48cd-45f7-8509-e1344b826a6c" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/004ac6fe-4541-4ce5-82b7-ccb3b05ce88b" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/ae886acf-0943-4b3c-b865-a58452fdf366" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/b02dad04-d3f0-4f6a-9c71-c6104a1fff6d" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/e6326adf-084f-4c4d-8dbb-2894210850c0" />


Results do not converge to <7%, as such third FEA is needed

<img width="500" alt="image" src="https://github.com/user-attachments/assets/0e4e9925-44c8-41c8-98bc-47c2a67a3dea" />


#### Fine mesh
<img width="500" alt="image" src="https://github.com/user-attachments/assets/c0aa9d7c-f1ed-473d-96fc-cf52b69251b3" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/e5bbfe56-3905-43af-be33-2d7065dcce13" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/83a7f180-8c41-4047-922f-b6e3c2d4077b" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/a35a03ce-ac68-4738-b253-795d51c3d555" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/7e5f1624-c504-42e6-8183-f4fa9c68fbbc" />





Because the minimum SF of 3 has yet to be reached, link will be made thicker, and gap between outer edge and hole will be increased

## Design 3

Increased thickness by 2 times, increased gap between holes and outer edge by 1.5x for a total of 3x the original length.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/c5a28dd0-b0e2-4fc8-9df9-e441ada9c136" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/f9002735-6531-416f-95b3-2078c92cf3a3" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/3f9eddc7-3a16-4d21-b128-761de51d25db" />


Mass is now 2.5lbs

<img width="500" alt="image" src="https://github.com/user-attachments/assets/05f771c5-1893-46ee-8ebb-19094987746c" />




#### Course mesh
<img width="500" alt="image" src="https://github.com/user-attachments/assets/67655e18-4d1a-4478-9fe5-e3831b7962e5" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/978a6c2a-5f06-43c3-b43c-255bcafc6bf3" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/d79db1e0-5549-4336-812a-095ab515fa3d" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/41558193-ff1c-4c81-8369-fb1449cbd357" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/0d0a4dbb-e7c4-424f-8acc-4edbcde5910b" />



#### Fine-course Mesh

<img width="500" alt="image" src="https://github.com/user-attachments/assets/e625e306-9dcd-434d-93d4-5b5130386c11" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/355a3097-0f50-4d73-b229-59aa6c363033" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/b3bd5a87-b135-449b-8ea7-82f127d0011e" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/fa75e085-5ab9-4d07-94d8-f46805617c32" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/b63a522d-3c92-4df1-9ee2-f1c2e3fb5676" />



Once again, results do not converge to <7%, as such third FEA is needed.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/0622483d-ac18-4079-89bf-0d7449541ed7" />



#### Fine mesh

<img width="500" alt="image" src="https://github.com/user-attachments/assets/bcc83f4c-10b2-4102-be04-dce3f2308220" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/50a0d494-a7e3-43da-8149-8e04b015a322" />

<img width="500" alt="image" src="https://github.com/user-attachments/assets/cfb465c7-319e-486d-8590-f45203e7dc10" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/2788b541-7bfa-4109-a146-430a035c1a4e" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/516d6a0b-7c25-4ec6-aaf3-47bd5b20cea9" />



With this design, although much heavier than the original, a satisfactory safety factor has been reached, as such the part is now complete.


# Download

[CAD Files and Excel Sheet for convergence %](https://drive.google.com/drive/folders/1vPD9U1M1VFhC9CN0d1bN3KWN8ZOfXZC3?usp=sharing)


































































