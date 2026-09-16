# A4 – Motor Mount

# Objective
The objective of this assignment is to design and analyze a motor mount for a 24 V DC gear motor while applying principles of beam bending, stress analysis, and deflection. The motor mount will be divided into two main features, and each feature will be analyzed as a beam to determine the required cross-sectional geometry. The design will first be evaluated based on yield strength using a safety factor of 3 and then checked to ensure that the maximum deflection does not exceed 0.30 mm at the free end.

ABS, PETG, or PLA will be selected as the material based on its mechanical properties and suitability for the application. Reasonable assumptions will be made to simplify the analysis while still representing the behavior of the actual mount. The calculated dimensions will then be used to develop a parametric CAD model of the motor mount. Additional features, such as ribs or gussets, will be considered to improve the stiffness of the design and reduce deflection.

Throughout the project, the design process will be documented through free-body diagrams, hand calculations, sketches, CAD models, design changes, and research into existing motor mount designs. The final design will demonstrate how analytical calculations can be used to determine practical dimensions and guide the development of a functional motor mount.


# Feature 1

I started this feature by first defining what I know and what I don't know.

<img width="436" height="218" alt="image" src="https://github.com/user-attachments/assets/b387edb4-cd31-4726-8b27-2c22045653af" />

I decided to define the length and the width of the feature and only solve for the thickness. This simplifies the calculations by leaving only one variable left to solve for. This also ensures that the motor will fit and have room to mount. I decide on a width of 37 mm as this made the mounting holes for the motor 6mm from the edge. I chose a distance of 6mm as it is roughly 2 times the hole diameter, this is a good rule of thumb I have picked up from parts I have deigned in previous projects. 

Now that I have defined what I need to solve for, I need to further define the problem with a free body diagram. Per the directions I defined feature 1 as a cantilever beam with the one end fixed and the recieving the force. 

<img width="204" height="112" alt="image" src="https://github.com/user-attachments/assets/3596de28-d056-4d64-adf8-cd02efba641c" />

The next step was to derive the equations for the beam yielding and for the deflection of the beam. This beam needs to be thick enough to not deflect too far but to also not yield. Therefore the minimum thickness will be the larger thickness given by the 2 equations. My derivation can be seen in the images below. 

<img width="409" height="380" alt="image" src="https://github.com/user-attachments/assets/30be60b3-6ebe-499a-89eb-2f3cf285fbcb" />

<img width="424" height="232" alt="image" src="https://github.com/user-attachments/assets/089fbca7-4d5b-4d76-94f3-44ee58c344f1" />

With the equations derived I then plugged in my known values and solved. I referenced SolidWorks for the material properties of ABS, the ensured if I ever needed to run FEA it would match well with my hand calculated values. I chose ABS for this part as it can withstand the highest temperatures of the other 2 options. This is important for a motor mount as we do not want the heat generated from the motor to soften the plastic and reduce its strength or rigidity. A thickness of 14mm was decided on based on the results of these equations. 

<img width="395" height="194" alt="image" src="https://github.com/user-attachments/assets/2e187a6d-541a-453f-a4ee-1ff76b34f6dd" />

# Feature 2 

The process of feature 2 was much the same as feature 1. I started by defining the knowns and unknows. 

<img width="418" height="187" alt="image" src="https://github.com/user-attachments/assets/d172a546-c8b5-4e67-9e60-f4ee98da4dd6" />

The width of this piece was pre-defined by the first feature as they mate together. I chose to make it a square so the length was equal to the width. 

According to the directions and the images in the appendix this piece was meant to be modeled as another cantilever beam, however this beam was meant to be supported at approximately 1/2 the length. This assumption can be seen in the free body diagram below. 

<img width="178" height="89" alt="image" src="https://github.com/user-attachments/assets/cb43d2ea-e268-496e-b2d7-212aad8a5763" />

I then derived the equations to describe this feature. The main difference between them and the equations for feature 1 is length is half the length of the part for the second feature. My derivation and solving can be seen in the image below. A thickness of 9.5 mm was chosen based on these equations. 

<img width="374" height="530" alt="image" src="https://github.com/user-attachments/assets/2cae2692-1834-4dfe-9016-8f84c8b34546" />

# Isometric Drawing 

Following calculating the thickness of the members I needed to plan out the part through an isometric drawing. I printed off some isometric grid paper to help me with this drawing. 

<img width="390" height="345" alt="image" src="https://github.com/user-attachments/assets/473e5d97-b29e-4de2-be51-a05cdb443d40" />

I discovered a few mistakes on this drawing after I started on the cad. The biggest if which was the drawn proportions between the thickness of the members and the lengths of them. This was way out of porportion on my drawing.

# Cad Moddel

I started my cad model by creating a new assembly and importing the cad model of the motor. I did this so later I could double check if my mount was correct. In the assembly I then created a new part for my mount and input my global variables and equation into the parts equation list. I then started feature 1 as a center justified rectangle centered on the origin. This fixed my part to the coordinate system helping to fully define the rest of my sketches. 

<img width="552" height="467" alt="image" src="https://github.com/user-attachments/assets/d5021d7f-2671-4ab2-8662-fdf56f4392a5" />

After extruding this part, I moved on to Feature 2 and modled it in a similar fassion. Creating a scetch on the bottom of feature 1 and then extruding.

<img width="839" height="661" alt="image" src="https://github.com/user-attachments/assets/bae108b7-8168-410d-add8-0ac9374e01c0" />

<img width="821" height="707" alt="image" src="https://github.com/user-attachments/assets/b84339a8-2418-4df8-95ab-fd54430bb6ca" />

Next, I went back to feature 1 and sketched the holes needed for the motor to mount and shaft to protrude. I had to inset the motor in to feature one some to ensure a usable about of the shaft sicks past. I created a construction geometry and center lines to define the location of some holes for the hole wizard in SolidWorks. 

<img width="867" height="628" alt="image" src="https://github.com/user-attachments/assets/b7374bb6-97c6-4b88-8402-ce25a35fb3e5" />

<img width="554" height="560" alt="image" src="https://github.com/user-attachments/assets/572a936c-5c85-4c18-a3b4-e1d2f7b2f6b7" />

After creating the screw clearence hoels for the motor it created some very sharp features where the holes intersected on of the indents that allow the motor to inset. I filleted these sharp points to improve ascetics and aid in maunfactuing the part. 

<img width="718" height="572" alt="image" src="https://github.com/user-attachments/assets/5f71e9be-60a0-46fc-81fa-f32d406141ef" />

Aditionaly I filleted the joint where feature 1 and feature 2 intersect to increase strength and prevent a stress concentration at this joint. 

<img width="657" height="621" alt="image" src="https://github.com/user-attachments/assets/00cdd65f-eeea-4c13-ab7a-55c720fca74c" />

With this design feature 1 takes up a lot of the top plane of feature 2. This became somewhat of a problem as there was no room for the forward 2 bolt holes. Because of this I decided to make these are blind holes with threads. This would allow the mount to still be mounted and prevent the need for nuts or other additional hardware during mounting. With threads like this this does limit the mount by requiring the bolts to be driven up from the bottom however with the motor installed this is the only direction the holes are accessible anyway. I chose to thread these holes as M4x0.7 at 10mm of debt. to ensure that that plastic can hold without tearing out I referenced and online thread pullout calculator. This calculated that each bolt threaded in at 10mm of depth into ABS can hold 1150 N of force. Our max load on the motor is only 300N therefore each bolt would be almost enough to hold the mount and keep our 3x safety factor. With 4 of these bolts installed this gives us a MAX tear out of 4600N or over a 15x saefty factor. 

<img width="695" height="703" alt="image" src="https://github.com/user-attachments/assets/fc407319-d73e-4fa4-9afa-80b44cde284e" />

<img width="902" height="680" alt="image" src="https://github.com/user-attachments/assets/253afbcc-9ea4-4391-bb8a-77cca6d3d4be" />

Now that my deign was created I imported the motor into the assembly and mated it to the mount. This allowed me to verify that my holes lined up and that no part of the motor was conflicting the mount. 

<img width="1045" height="584" alt="image" src="https://github.com/user-attachments/assets/b1f0646a-e91f-4465-aebe-90327b8c1fad" />

<img width="601" height="537" alt="image" src="https://github.com/user-attachments/assets/87cb7830-2a51-4575-b2cd-8eb716b87aeb" />

Below is the link to my cad model
https://github.com/JacBinon/SOHPMORE-DESIGN/blob/main/docs/assignments/A04/A4%20Assembly.zip

# Drawing 

I created a A sized drawing for my part below is an image of this and the link to the full pdf.
https://github.com/JacBinon/SOHPMORE-DESIGN/blob/main/docs/assignments/A04/Drawing%20A-4.pdf.

<img width="731" height="565" alt="image" src="https://github.com/user-attachments/assets/88793205-8d58-4b3b-b5a7-44caa1ed4fc1" />

# Time

I estimate I spent 5 hours on this assignment. 








