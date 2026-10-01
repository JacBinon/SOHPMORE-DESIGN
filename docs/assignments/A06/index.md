# A6 – Bracket Drawing

# Parametric Design 
For my design I decide to use the strength equations from the last assignment. These all required larger dimensions therefore both criteria would still be satisfied. I did this by first making a new SolidWorks part and in the equations defined all my knowns and then solved for all my unknowns' using equations. This allowed my entire model to change if one of the dimensions or criteria changed. 

<img width="1565" height="768" alt="image" src="https://github.com/user-attachments/assets/c3fa74e2-f92f-4103-9018-9eaf93dab70b" />

After defining all the equations, I defined the cad model using only those dimensions and references. 

<img width="747" height="710" alt="image" src="https://github.com/user-attachments/assets/1ed61fa5-e877-4c18-8944-eb7456bebf72" />

# Drawing 
Now that my model had been created, I needed to create and engineering drawing to fully tolerance this design. 

<img width="1196" height="927" alt="image" src="https://github.com/user-attachments/assets/e4415255-773f-4080-9b60-38f871b567be" />

You will notice the double plus tolerances in this drawing. This was done to ensure that the features were designed to the nominal dementias required for strength but were still able to ensure at the extreme ends of the tolerance range that a proper fit was still maintained. This fit class was derived from a combination of A5 instructions, the tolerance on the beam this attaches too, and the Running and sliding fit tables in my machinery's handbook. Additionally, many of the dimensions are -0 +x.xxx this was done to ensure the features were at minimum the same size if not larger than what the equations called for. A tolerance block was also included for less critical tolerances. The RC fit callout is mainly a approximations as denoted under the tolerance box. This is an approximation because the range of possible clarence between the 2 features falls withing the denoted class fit, but the tolerance range on the beam is different. In other words in the table the tolerances are mainly for hole and shaft fit but have been adapted for the irregular geometry of these features. I chose and RC 3 for the width as the instructions called for "the closest fits that can be expected to run freely". The small slot on the top was an RC 5 as that tolerance was described as "intention for use where accuracy is not essential". Lastly the height was between the 2 of these being a RC 4 "is where accurate location and minimum play is desired". I extrapolated the maximum and minimum dimentiuons of the t beam that atatechs to this feature and used that to gauge what fits were possible and right. 

<img width="1021" height="512" alt="image" src="https://github.com/user-attachments/assets/193e0c2f-e2d9-4024-ab8d-681536bef1cf" />

# Reflection
Defining the model complety parametrical was fairly straightforward. I simply coppied the algebraic solutions I defived from last assigment in to the equation block. I then siply input known vlaues as global variables. However I did get stummped at one point, when I needed to use a cube root I could only find square root. It took me a few minutes to rember that roots can bes descrived as an exponet fraction, so I put the equation to the power of 1/3. Over all this was a straigh forward process. Changing parpparameters does update the entire moddel. In the immage below all I changeds was the load and the entire moddel updeated. 

<img width="1022" height="802" alt="image" src="https://github.com/user-attachments/assets/bff28c24-accb-439a-b70f-6b3ea6fb8b04" />

Reflecting on my design I came to the realizations that the assumptions I made when initially solving were a bit too broad. For the memberes I assumed were simply an axily loaded beam they seem far to thin to resist the bending moments through them. If I were to re do this assigment I would moddel them as a cantiliver beam with a moment at the end or as a beam loaded on each end supported at the middle. 

One place I put a tighter tolerance was on the overall width of the inside slot. 

<img width="1177" height="632" alt="image" src="https://github.com/user-attachments/assets/556b7e17-1556-4110-a88c-dd7a9cbe2446" />

I placed the double plus to ensure that no matter what there was some clearance between the part and the part it slides on. I found the limits of the tolerancy by taking the bigest one side could be and caluating what the smallest the other could be while still having the minium clearence of that calss of fit I was aiming for. I then took the smallest one side could be and the biggest the other could be and calulated what the upper limit could be basued again on the max clearance based on the fit table. I did this process for all the precise fits on this project. 

# Link Design

## Parametric Cad
I started this cad much like the previous part. This time I used the deflections calculation as it yielded a larger cross section in the previous assignment. I input my knowns and solved for the unknown, in this case the thickness of the part. 

<img width="1567" height="737" alt="image" src="https://github.com/user-attachments/assets/3292f4e3-ef0d-4145-97af-6b3197cea6e3" />

<img width="841" height="736" alt="image" src="https://github.com/user-attachments/assets/22712f61-a5b1-475a-b736-6271469127f2" />

I chose to set the center toc enter distance of the 2 holes at an arbitrary distance of 2 inches. Additionally, I mad ethe distance from the edge of the hole to the edge of the part a constant .125 inches as well. This allowed me to only have one variable to solve for, the thickness of the part. Setting that distance also meant that my smallest cross sectional would be easy to solve for and define. 

## Drawing

Below is my Drawing of the Link Part. I referenced the tolerance table to get the correct toleracnes for the hole feature for the required class of fit. The fit class is noted below the dimention. The fit standard being refrenced is defined under the tolerace table. 

<img width="1201" height="927" alt="image" src="https://github.com/user-attachments/assets/02a785da-7ced-49e2-b13e-6b21cbe066ac" />

## Reflection

One lesson I learned from this assignment pertaining to designing parts with specific fits is you need to take in to account this tolerance in the overall dimensions of your part. This is mostly the case for fits where you have a minimum spacing between If you modeled the parts like I did where they are both the same size only off by a small amount once you add the tolerances you could run into issues if your minimum gap as larger say 10 or 15 thousandths instead of the 1 to 2 I had. 

Defining tolerances like this makes you think a lot more about how you want your part to function. You must be intnetional with the toleracnes you give your parts especialy at joints and areas where mroe than one part interact. You also have to think about how the adding up of tolleacnes accorst multiple parts may effect your over all assembly. Take a pair of issors for example. On one blade the pivot pin can be super tight as long as the other one is loose, but if its too losse they wont work. If the blades of the sissors are too thick your cneter pin may not even be long enough. Toleracnes are equaly as important as the nominal dimentios of parts. 



