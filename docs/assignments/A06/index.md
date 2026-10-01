# A6 – Bracket Drawing

# Parametric Design

For my design, I decided to use the strength equations from the last assignment. These all required larger dimensions, so both criteria would still be satisfied. I did this by first making a new SolidWorks part and, in the equations, defining all my knowns and then solving for all my unknowns using equations. This allowed my entire model to change if one of the dimensions or criteria changed.

<img width="1565" height="768" alt="image" src="https://github.com/user-attachments/assets/c3fa74e2-f92f-4103-9018-9eaf93dab70b" />

After defining all the equations, I defined the CAD model using only those dimensions and references.

<img width="747" height="710" alt="image" src="https://github.com/user-attachments/assets/1ed61fa5-e877-4c18-8944-eb7456bebf72" />

# Drawing

Now that my model had been created, I needed to create an engineering drawing to fully tolerance this design.

<img width="1196" height="927" alt="image" src="https://github.com/user-attachments/assets/e4415255-773f-4080-9b60-38f871b567be" />

You will notice the double-plus tolerances in this drawing. This was done to ensure that the features were designed to the nominal dimensions required for strength while still ensuring that, at the extreme ends of the tolerance range, a proper fit was maintained. This fit class was derived from a combination of the A5 instructions, the tolerance on the beam this attaches to, and the Running and Sliding Fit tables in my Machinery's Handbook.

Additionally, many of the dimensions are -0 +x.xxx. This was done to ensure the features were, at minimum, the same size as required by the equations, if not larger. A tolerance block was also included for less critical tolerances.

The RC fit callout is mainly an approximation, as denoted under the tolerance box. This is an approximation because the range of possible clearance between the two features falls within the denoted class fit, but the tolerance range on the beam is different. In other words, in the table, the tolerances are mainly for hole and shaft fits but have been adapted for the irregular geometry of these features.

I chose an RC 3 for the width because the instructions called for "the closest fits that can be expected to run freely." The small slot on the top was an RC 5 because that tolerance was described as "intended for use where accuracy is not essential." Lastly, the height was between the two of these, being an RC 4, which "is where accurate location and minimum play is desired." I extrapolated the maximum and minimum dimensions of the T-beam that attaches to this feature and used that to gauge what fits were possible and appropriate.

<img width="1021" height="512" alt="image" src="https://github.com/user-attachments/assets/193e0c2f-e2d9-4024-ab8d-681536bef1cf" />

# Reflection

Defining the model completely parametrically was fairly straightforward. I simply copied the algebraic solutions I derived from the last assignment into the equation block. I then input known values as global variables. However, I did get stumped at one point when I needed to use a cube root, but I could only find square root. It took me a few minutes to remember that roots can be described as an exponent fraction, so I raised the equation to the power of 1/3. Overall, this was a straightforward process. Changing parameters does update the entire model. In the image below, all I changed was the load, and the entire model updated.

<img width="1022" height="802" alt="image" src="https://github.com/user-attachments/assets/bff28c24-accb-439a-b70f-6b3ea6fb8b04" />

Reflecting on my design, I came to the realization that the assumptions I made when initially solving were a bit too broad. For the members I assumed were simply axially loaded beams, they seem far too thin to resist the bending moments through them. If I were to redo this assignment, I would model them as a cantilever beam with a moment at the end or as a beam loaded on each end and supported at the middle.

One place I put a tighter tolerance was on the overall width of the inside slot.

<img width="1177" height="632" alt="image" src="https://github.com/user-attachments/assets/556b7e17-1556-4110-a88c-dd7a9cbe2446" />

I placed the double-plus tolerance to ensure that there was always some clearance between the part and the part it slides on. I found the limits of the tolerance by taking the largest one side could be and calculating how small the other could be while still having the minimum clearance of that class of fit. I then took the smallest one side could be and the largest the other could be and calculated what the upper limit could be based again on the maximum clearance from the fit table. I did this process for all the precise fits on this project.

# Link Design

## Parametric CAD

I started this CAD much like the previous part. This time, I used the deflection calculation because it yielded a larger cross section in the previous assignment. I input my knowns and solved for the unknown, in this case, the thickness of the part.

<img width="1567" height="737" alt="image" src="https://github.com/user-attachments/assets/3292f4e3-ef0d-4145-97af-6b3197cea6e3" />

<img width="841" height="736" alt="image" src="https://github.com/user-attachments/assets/22712f61-a5b1-475a-b736-6271469127f2" />

I chose to set the center-to-center distance of the two holes at an arbitrary distance of 2 inches. Additionally, I made the distance from the edge of the hole to the edge of the part a constant 0.125 inches as well. This allowed me to only have one variable to solve for: the thickness of the part. Setting that distance also meant that my smallest cross section would be easy to solve for and define.

## Drawing

Below is my drawing of the Link Part. I referenced the tolerance table to get the correct tolerances for the hole feature for the required class of fit. The fit class is noted below the dimension. The fit standard being referenced is defined under the tolerance table.

<img width="1201" height="927" alt="image" src="https://github.com/user-attachments/assets/02a785da-7ced-49e2-b13e-6b21cbe066ac" />

## Reflection

One lesson I learned from this assignment pertaining to designing parts with specific fits is that you need to take these tolerances into account in the overall dimensions of your part. This is mostly the case for fits where you have a minimum spacing between features. If you model the parts like I did, where they are both the same size and only offset by a small amount, once you add the tolerances, you could run into issues if your minimum gap were larger, say 10 or 15 thousandths, instead of the 1 to 2 thousandths I had.

Defining tolerances like this makes you think a lot more about how you want your part to function. You must be intentional with the tolerances you give your parts, especially at joints and areas where more than one part interacts. You also have to think about how the accumulation of tolerances across multiple parts may affect your overall assembly.

Take a pair of scissors, for example. On one blade, the pivot pin can be super tight as long as the other one is loose, but if it is too loose, they will not work properly. If the blades of the scissors are too thick, your center pin may not even be long enough. Tolerances are equally as important as the nominal dimensions of parts.

# Files 
Below are all the files for this assignment



