# A3 – Parametric and FEA 

# Objective
The main objective of this assignment is to understand how load, geometry, and material properties affect the stiffness and deflection of a structural bar. I will design an aluminum bar with a circular cross section that meets a specified maximum axial deflection under a direct tensile load.

I will use the axial deflection equation to determine the required length of the bar and then use parametric modeling in CAD to link the load, material properties, deflection, and dimensions to the final design. After creating the bar, I will use FEA to analyze its deflection and von Mises stress under the same loading conditions.

Finally, I will compare the hand calculations to the FEA results to determine how closely they agree and evaluate whether the design meets the required strength and safety factor. The assignment will also show how changing parameters such as load, width, height, and thickness affects the resulting design.

# Analyze

## Defining Problem 
The Directions state "You are to design a bar which has a circular cross section where the values of the criteria given for the material, maximum deflection, and load. Determine the bar’s minimum geometry (ie.. length, diameter, and weight) through parametric design while under direct tension. Then verify the geometry through finite element analysis." And gives the following figure to further define the task: 

<p align="center">
<img width="748" height="154" alt="image" src="https://github.com/user-attachments/assets/6e1b893a-e318-4af8-96b0-07180ce20c6c" />
</p>

From this Figure I gathered that the bar will need to be fixed at one end and the force is "stretching" the bar along it's length. Aditonaly I knew this bar will be a cylinder absed on the directions specificity of a circu;art cross sections. I then drew this diagram to help visualize the senario.

<p align="center">
<img width="1466" height="307" alt="image" src="https://github.com/user-attachments/assets/d264a0c3-2a41-4fef-9b48-2f91c0aa49a5" />
</p>

The next thing I did was to define the a;umiunm I was going to be using. The directions stated to use an alloy with a modouu of eleacticty between (8.5 - 11.5) x 10^6 psi. To help the accuracy of my hand calulations later I wanted to use the numbers defined by a material in Solidworks. This led me to use 7075-T6 as my material. I have peronaly worked with this material before and its modoulus of elacticity fell inside the range. I further confiemed this number by refernec MATT.WEB to ensure the numbers were the same. 

<p align="center">


<img width="1368" height="985" alt="image" src="https://github.com/user-attachments/assets/fc190a8c-73af-4e2d-b957-35ce6860cb73" />

<img width="1485" height="752" alt="image" src="https://github.com/user-attachments/assets/28bbd978-5405-4a93-a595-d65a42aafff2" />


</p>

Lastly I needed to define what eqations I needed to use for my elongation calcualtions. I found this eqauton form my macheneries handbook. This equation will be used as part of my parametric cad and my hand calculations. 

<p align="center">
<img width="1651" height="702" alt="image" src="https://github.com/user-attachments/assets/5dacc37c-67c3-4115-83df-4b6b1eaabded" />
</p>

# Decide
## CAD and FEA 

I strted my cad by first defining the parametric equations that will determine the dimentions of my bar. I named these easily identifyable variables. 

<p align="center">
<img width="2422" height="1187" alt="image" src="https://github.com/user-attachments/assets/1abe1479-eff3-4ef3-812e-44b64845cb3c" />
</p>


I then created a scetch and used these numbers to define the diameter and then to define the length of the extrusion, this created my final bar.

<p align="center">
<img width="1825" height="1215" alt="image" src="https://github.com/user-attachments/assets/bfb5a619-791a-4274-91a5-332ae86078e6" />

<img width="2777" height="1333" alt="image" src="https://github.com/user-attachments/assets/849e18b7-1df1-4bfa-9af0-4e8ec2f79df6" />

<img width="2542" height="1236" alt="image" src="https://github.com/user-attachments/assets/84006d3a-2f36-4d7f-ac9d-97f1da7b7602" />

</p>

Now that my bar has been created, I defined my fixture and loads for my FEA analysis. I fixed one face of the cylinder and on the opposite face applied my force of 400LBs distributed along that face. 

<p align="center">
<img width="1418" height="887" alt="image" src="https://github.com/user-attachments/assets/8f00859c-91f6-4a79-ad7b-7bc5836655ee" />
<img width="2017" height="991" alt="image" src="https://github.com/user-attachments/assets/4306ceec-db66-4aaf-b826-7eeb667c56b0" />

</p>

Now that my Bar has been created in cad and fixtured in the FEA simulation I ran the simulation and documented the deflections and max stress.

<p align="center">
  VonMises/Stress
<img width="2586" height="1506" alt="image" src="https://github.com/user-attachments/assets/b53f7f9f-afd9-47f6-bb46-bff5d6be223a" />
<img width="2592" height="1500" alt="image" src="https://github.com/user-attachments/assets/9eed136f-c1c9-4a92-b74b-2fbc9219c5d1" />
<img width="2570" height="1498" alt="image" src="https://github.com/user-attachments/assets/10169b81-f350-45ff-baa9-904162693c9b" />

  Displacement/Deflection
<img width="2577" height="1507" alt="image" src="https://github.com/user-attachments/assets/d346cd5e-c46b-4911-9b11-af962deb972e" />
<img width="2578" height="1497" alt="image" src="https://github.com/user-attachments/assets/6dec59ac-2bc7-4751-9f2f-3a5c3ad2b876" />
<img width="2566" height="1495" alt="image" src="https://github.com/user-attachments/assets/651ddce6-b3e4-46f2-95ea-0c9173a23a73" />
</p>

With a Max Stress defined as 5.475.10^-1 this leaves a saefty factor of 73.1 assuming a Sy=40 KSI

<p align="center">
<img width="1528" height="383" alt="image" src="https://github.com/user-attachments/assets/dd0ff16a-673d-4e26-bcc4-992560a13aa3" />
</p>

## Hand Calculations and Comparison To FEA

Now that I had Ran FEA on the beam, I need to conduct hand calculations to compare against the deflections seen in the model. I used the elongation equation previously gathered for machineries handbook for this calculation.

<p align="center">
<img width="1568" height="832" alt="image" src="https://github.com/user-attachments/assets/69d9ff0c-ae72-4794-b329-95b78c5dfa52" />
</p>

This showed a hand calcualted value of 0.009" of defelction. My FEA had a max displacement of 0.009013". This equates to a present difference of 0.144%. This Is an insignifficant differne. It is insignigfcant for one becasue the present differnece is extremily small, but also insignificant because a differnce of 0.000013" is magnitudes smaller than the manufactuing tolernace of most parts and is imeasurable without specilized tools and controled temperatuers. For the pourpose of this assigment this differnce is basically 0. I belive that these values are so simmilar beacuse I am using the same material porperties in my hand cacluations as solidorks is. Aditonaly this is a very simple loading with no bending only stretching simplifying the hand calculations. The Geometry is also very simple. These factors combied are what I believe causes tese values to be so simmilar. In the case of this aplication I would trust the hand calulations over the FEA as the geomety is simple enough to do. howver on a more complex part with more complex forces I may be inclined to trust the FEA over my own math. I do fell it is still important to check your fea values againt some hand caluations even if it means simplyfing the geometry or loading some just to make sure your in the right ball park. 

## Pin Hole Cenario 

The directions state to imagine a "substantial" pin hole in the end of the bar and to use the Peterson's charts or Machinery's Handbook to estimate the peak stress at the hole with the nominal stress in the bar. I chose to use a hole with the diameter of 0.5" or half the diameter of the bar. With an nominal stress of .506 KSI, and a Kt of about 2.1 from the chart we get get a peak stress of 1.01 KSI. Assuming a Sy=40KSI this gives us a safety factor of 37.7. This is well withing a safe range. 

## Communicate

## Modifying Design Parameters

As instructed, I will be changing each of the design parameters and predicting if the parametrically defined length of my beam will change. I was Instructed to change the load, thickness, height and width. As my bar has a circular cross section I will change diameter instead of height, width, and thickness. 

-Change in Diameter:
  I chose to change the diameter from 1" to 2". I think this will make the bar longer as there is more material to resist the stretching force so the bar can be made longer before it will reach the max diflection.

-Change in Load
  I chose to increase my load from 400LBS to 800LBS. I believe that increasing the load will shorten the length of the rod as there is more force so the material will stretch more meaning the bar needs to be shorter to not surpass the maximum deflection. 

<p align="center">

Control
<img width="2365" height="457" alt="image" src="https://github.com/user-attachments/assets/56d1fc74-dc0f-4452-acd8-28ac9d89d9cf" />

Change to 2" Diameter
<img width="2347" height="506" alt="image" src="https://github.com/user-attachments/assets/d7c11e06-9018-487e-80e0-e1e15a48c800" />

Change to 800LB Force
<img width="2355" height="492" alt="image" src="https://github.com/user-attachments/assets/9084bd75-b185-4914-8b17-f34976db9e2e" />
</p>

My predictions were correct with the 2" diameter the length of the bar greatly increased and with the 800lb force the length of the bar greatly decreased.

## Time taken
I estimate this assignment took about 3.5 hours. I am familiar with SolidWorks and FEA within it making the cad portion of this assignment easy. 

## Link to CAD
https://github.com/JacBinon/SOHPMORE-DESIGN/blob/main/docs/assignments/A03/Sophmore%20Design%20A3.SLDPRT


