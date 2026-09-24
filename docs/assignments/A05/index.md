# A5 – Bracket

# Objective
The objective of this assignment is to design a bracket capable of safely supporting a horizontal load while applying principles of statics, strength of materials, stress analysis, and deflection. The bracket will be divided into individual features, and each feature will be analyzed using free body diagrams, known and unknown variables, assumptions, and algebraic models to determine the required dimensions. A safety factor of 4 will be used with a selected metal material, and the applied load will be traced through each feature so that the reaction forces from one feature can be used as the loading conditions for the next. Both strength and stiffness will be considered, with stress analysis used to prevent material failure and stiffness analysis used to keep deflection within the specified 0.005 in limit. The results from both analyses will then be compared to determine which requirement governs the final dimensions. This assignment is intended to demonstrate how fundamental engineering equations can be used to develop a safe and functional component from a conceptual design while considering material properties, loading conditions, assumptions, and design constraints.

# Defining the Problem 
I started by drawing out what I needed to design and defined my material. I chose 6061T6 as I have used it before and it's easier to machine than for example titanium. 
<img width="735" height="962" alt="image" src="https://github.com/user-attachments/assets/8c15ebec-1a2e-485d-b4a3-c1351b9ac3b8" />

# Strength and Deflection Calculations
After defining my problem, I then started on all the math for this assignment. I initially started with part E but realized I needed dimensions defined by other parts to finish. After taking another look at the problem I then started with A then B then D, E, and finished with C. My assumptions and rational for models are included in the paperwork for each feature. 

<img width="932" height="1212" alt="image" src="https://github.com/user-attachments/assets/069ca8c3-f548-421b-9415-339b3f33dd68" />
<img width="770" height="1006" alt="image" src="https://github.com/user-attachments/assets/08fa4f41-3542-4ff8-b83d-6b5a00c946b2" />
<img width="811" height="1115" alt="image" src="https://github.com/user-attachments/assets/e6ddcf79-44e5-4133-b75e-8ca463eaae47" />
<img width="735" height="966" alt="image" src="https://github.com/user-attachments/assets/168abd29-be07-4e58-b398-a3a62fa2621b" />
<img width="740" height="987" alt="image" src="https://github.com/user-attachments/assets/53032ea3-34b5-4092-bd5a-7e2823647d78" />

# Multi View Drawings
After defining the dimensions, I created 2 distinct 3 view drawings. One used the dimensions given from the strength of the aluminum and the other from the deflection. This allowed me to further see how these 2 failure modes are connected.

<img width="771" height="591" alt="image" src="https://github.com/user-attachments/assets/ebbe67d6-9f66-4466-99a9-e6a3083b04fb" />
<img width="861" height="658" alt="image" src="https://github.com/user-attachments/assets/9067b6bd-c937-4b86-8323-f3950fbc0461" />


# Analysis 
4. Comparing the numbers all of the features required the dimensions from the stress equations, however for feature C the two were very close. The dimensions were within 60 thousandths of each other.
5. One place that I made and error and caught it was while solving my stress equation on feature E. In the numerator I had the correct numbers, but in the denominator, I had the deflection numbers. Fortunately I caught this before solving and moving on. This would not have affected my math for any of the other features, but it may have caused the entire mount to fail under load.
6. One assumption I made was assuming that the cylinder the strap on was a cantilever beam with the load on then tip. I chose this one over the distributed load to prevent failure in the event the strap slipped down the feature. If I were to choose the distributed load this feature would end up thinner. I decided it was best to design for the worst case scenario.

# Fits Feature
I started designing the linkage by defining my stress and deflection equations as well as hole sizes. I also defined the center-to-center distance of these 2 holes as 2". Below is my work for this feature. I only solved for the minimum cross-sectional area not all of the dimensions of this piece as the directions did not call for them. I assumed the smalless cross sectional are would occur next to each of the holes. 

<img width="1106" height="1507" alt="image" src="https://github.com/user-attachments/assets/66d442cb-07b4-4960-831b-512025098263" />

For defining the fits, I consulted the machineries handbook. I chose a RC4 fit for the feature A interface as this was one of the closer running fits. This would help prevent excessive slop in the interface and hopefully prevent the linkage form sliding off as easily under load. 

<img width="969" height="560" alt="image" src="https://github.com/user-attachments/assets/5299580e-4a8e-469c-b064-c0bc7ba5a80c" />

For the 1 Inch shaft I chose a FN1 fit. This would give a light press on fit. Going with a looser press fit also ensured the tolerance required were reasonable. Choosing a light press fit also ensures assembly is easy, more aggressive fits would require extreme force or freezing temps to assemble. 

<img width="1055" height="655" alt="image" src="https://github.com/user-attachments/assets/0d29f29e-3b93-489b-bf18-17f49addcf11" />

For both of these fits reaming would provide the necessary tolerance, surface finish, and concentricity. 

<img width="585" height="1116" alt="image" src="https://github.com/user-attachments/assets/20b50f7b-7613-4b19-83ee-588634ca7a51" />

As shown reaming can achieve a class 6 tolerance which is adequate for the hole diameters. Reaming is also relatively easy to do in any machine shop provided the correct size reamers have been acquired. 



