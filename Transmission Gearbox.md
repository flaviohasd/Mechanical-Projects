# Disclaimer
  This project was developed as a form of evaluation for the subject Machine Elements II in the Mechanical Engineering course at the Federal University of Amazonas in july 2021. The two authors were Rodrigo Nascimento and myself, Flávio Dias.

# TWO-SPEED TRANSMISSION GEARBOX

## INTRODUCTION
  Life on earth depends on energy and work. Since ancient times, mankind has looked for ways to generate, transmit, and store work, to make everyday activities easier, such as grinding grain using wind power in medieval times, or to perform some extraordinary feats, such as racing cars that go from 0 to 100 km/h in two seconds. Whatever the application, it is essential to change the transmission ratio of the system, that is, to adapt the way this energy is used so that it has more torque when it is needed and more speed when it is not.

  This paper aims to design one of the methods that allows this flexibility, the gearbox, a set of machine elements whose function is, as the name suggests, to transmit speed, force, torque and power in the desired proportions. Mechanical energy from the source is conducted through a shaft (driven shaft) and through a series of gear ratios this mechanical energy is supplied to the output shaft (driven shaft).

  The main advantage of this transmission model is the ability to transmit large magnitudes of power ( in the case of "heavier" applications) with high mechanical efficiency and precise synchronization, and it can be built from durable materials without the need for periodic adjustments.
  
  The design of a complete gearbox consists of defining the dimensions of all elements (listed below), material specifications, and analysis of forces and resistances. Based on the understanding of science and mathematics, combined with the knowledge of empirical data together with "engineering judgment", to develop the design as a professional solution. Some of the most common elements in this type of design are:
  
  - The gears, responsible for transmitting the rotational motion from one shaft to the other. They are generally more expensive than chains and belts, since manufacturing costs increase with precision - required in the combination of high speeds, loads, and low noise levels.
  - The shafts, which transmit the power to the elements attached to it (pulleys, cams, and - in this case - gears), are generally long with circular section and supported by bearings.
  - The bearings, which support rolling elements, the shaft, and the outermost components are separated by balls or rollers that allow relative movement between them.
  - The fastening elements, with the purpose of coupling neighboring components, allow the transmission of torque and speed, and also serve as a fuse in case of overload.
  
  Besides the correct dimensional analysis, the material is also of fundamental importance, because it is through the material that the internal forces of deformation and resistance are tied. The optimal choice makes the manufacturing process easier to perform and reduces the system cost. Therefore, it is important to balance these variables.
  
  Since different approaches can be taken to achieve the same result, caution in component sizing and decision-making must be carefully considered so that the design, although not the only one and perhaps not the best, is acceptable within the limits of cost, manufacturing time, and dimensions.
  
  The shifting concept in this work was based on a formula 1 car transmission model, and the design was developed knowing only the graphs of the speed vs torque/engine power ratios, overall efficiency of the transmission system, wheel/tire dimensions, and inertia characteristics of the vehicle to be driven.
  
  The details of the decision-making (and its motivations) for each stage of the project have been described in the following chapters, along with the figures used, organized mostly in tables for ease of viewing.
  
  
  ## OBJECTIVES
  
  The main objective is to design a two-speed gearbox, with at least two gear pairs, and all its components (housing, gears, shafts, fasteners - with the exception of the bearings, chosen from a catalog) from the requirements given, making design decisions independently and, when necessary, using auxiliary software in order to facilitate the iterative calculations.
  
  The goal set was to design as few components as possible, using the cheapest materials (in this case alloy steel), with the smallest possible dimensions (without ignoring desirable profiles, as in the case of the staggered shafts) and to achieve acceptable speeds and torques at the output of the system. With the construction and assembly of the components made as simple as possible.
  
  The following sequenced steps below were followed for sizing the speed ratios and component planning:
  1. Establish appropriate gear ratios for the system, taking into account the limitations of the engine providing reasonable speed and torque output for a vehicular application;
  2. Design the gears that can withstand stresses without fatigue failure for an established lifetime;  
  3. Design the shafts where the gears will be coupled, also following the fatigue resistance criteria;  
  4. Define the requirements for the bearings (based on the previous steps) and select them from a commercial catalog;  
  5. Design the fasteners or the type of fit between bearings/gears and shafts;  
  6. CAD design of all components.
  
  
   ## CALCULATION MEMORIAL
   
   ### SPEED CHANGE
   
   Most of the project's calculations were performed in Microsoft Excel. Given that iterations and modifications of the project are expected during the course of development, this tool was extremely useful.
   
   Since these are repetitive calculations for similar components, it was preferred to organize the data in tables along with the results to facilitate the visualization of each step.
   
   Before entering the calculations, the following initial concepts helped visualize the desired scheme:
   
<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198148113-b5f0c2ef-8d21-486a-a505-20e85d5f0be4.png" width=50% height=50%>
</p>
<p align="center">
Fig. 1 - Transmission scheme
</p>

In Fig. 1 are organized the references of each of the component that will be cited throughout the work.

The above model was not the first one planned. Initially it was tried to obtain acceptable linear vehicle speed results without the first reduction (a-b shaft / gear 1-2) but without success, as the component dimensions for such an application were unfeasible (gears with absurd diameters). The addition of an initial reduction before the gear shifting system solved the problem for this condition.

With the model well defined, the need was seen to "recalculate" the torque and power curves to obtain with greater confidence intermediate scale values of the graph provided. To do this, the Wolfram[^1] software was used, in which the inputs are the most accurate data that could be visually extracted from the speed x torque/power graphs.

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198149778-e39f94de-da2a-4b66-8238-997ca8cf210f.png" width=50% height=50%>
<img src="https://user-images.githubusercontent.com/44821460/198149918-f556ff38-0a33-487b-86ed-7e12a5b0671a.png" width=50% height=50%>
</p>
<p align="center">
Fig. 2.1 - Power vs RPM curve
</p>
 
 [^1]: Available online at: https://www.wolframalpha.com
  
  The curve that best fits the input points (has the highest R²) in this case is the quadratic curve. Therefore, the quadratic equation provided will be the one used to reconstruct the power graph curve.
  
  
<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198150356-84b15409-dc09-4d9f-8bf1-094e6d8b2b55.png" width=50% height=50%>
<img src="https://user-images.githubusercontent.com/44821460/198150369-6c54be0d-884a-4c53-a89a-e40c8460f127.png" width=50% height=50%>
</p>
<p align="center">
Fig. 2.2 - Torque vs RPM curve
</p>

For the case of torque, the best-fitting curve is the cubic curve. This was then used to reconstruct the graph.

From the values of interest for the tire, the diameter is 560 mm, and the overall moment of inertia of the system to be moved is 21.5 kg.m².

And with the input values (axis a) better calculated, from the equations obtained, some gear ratios were arbitrarily chosen (in the case shown: 4, 4 and 2 - see later to understand why these values were chosen) to visualize the torque and speed in the other axes (axis b and c), obtaining the following table:


<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198152122-85ff3e5d-7398-4bde-8529-e1bb7a738793.png" width=80% height=80%>
</p>
<p align="center">
Tab. 1 - Torque and angular shaft speed
</p>

Note: Knowing the required overall efficiency of the system (97%), the efficiency per torque step was set at 98.5%, which generates a difference of only 0.0225% of the required value.

From Tab. 1, "Max" represents the value of the maximum torque (N.m) for that shaft and its respective angular speed (rpm) at which both occur at the maximum point of the motor torque curve. These will be the critical values that the components planned further on must withstand.

It is worth mentioning that for this analysis the scenario where the engine speed was reduced below the proposed minimum (2000 rpm) was disregarded, so the initial car speed could not be considered 0 and the clutch effects initially required for this condition were also disregarded.

From this table, the required system accelerations were estimated following the following logic:

- Gear 1: from 13.2 km/h to 26.4 km/h in how long?
- Gear 2: from 26.4 km/h to 52.8 km/h in how long?
- Answer: 5 and 42 seconds, respectively. Considering that the first gear should be able to provide the highest torque, it is not necessary to reach high speeds, because the goal is to overcome the initial inertia. For the second case, it is not necessary to have a large torque, because the vehicle will already be moving and the time to reach maximum speed may be shorter.
With these data we obtain the angular accelerations (simplified as constant, because it is an average variation of the speed) required by the system and the torque required for the application (M).

$$ 𝑎 = {𝛥v \over 𝛥𝑡} → 𝛼= {𝛥ω \over 𝛥𝑡}, 𝐹=𝑚𝑎 → 𝑀=𝐼𝛼= 𝐼{𝛥ω \over 𝛥𝑡} $$

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198154344-db157411-6138-4bba-8755-b648310fe6ed.png" width=50% height=50%>
</p>
<p align="center">
Tab. 2 - Required accelerations and moments
</p>

From this, several tests were performed by varying the gear ratios initially chosen in order to obtain values of M_min that were surpassed by all torque values of the output shaft (being limited to the engine speed range, ensuring that the output torque would always be able to accelerate despite the load) and had reasonable values. Therefore, the ratios chosen were 4, 4 (gear 1) and 2 (gear 2).

To visualize the range of motor speed vs. linear speed, along with the zone of optimal torque and power, the graph below has been drawn:

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198155170-c193659b-8318-4d94-8111-9ffeddc2acc5.png" width=50% height=50%>
</p>
<p align="center">
Fig. 3 - RPM vs Velocity Chart
</p>

With the gear ratios defined and all criteria met, the gear design can begin.

 ### GEAR DESIGN
 
 The design began with the definition of the number of teeth of the pawl of the first gear (gear 1). To do so, the following equation was used for the minimum number of pawl teeth without interference, according to Budynas (2011, p. 692):
 
 $$𝑁_{𝑝} = {2𝑘 \over (1+2𝑚)𝑠𝑒𝑛²𝛷}(𝑚+\sqrt{𝑚²+(1+2𝑚)𝑠𝑒𝑛²𝛷} )$$
 With k = 1 (for full-height toothed gears) and 𝛷 = 20°.
 
 The result of this first equation returns 15.44, rounding to 16 gives the number of teeth for the first gear. The gear that makes a pair would thus have 64 teeth. Since the second pair of gears (3 and 4) have the same transmission ratio, one can take advantage of these values.
 
 To proceed, it was established that the distances between centers should be equal for all gears (basically analyzing the scheme initially assembled, shown right at the beginning of the work - Figure 1). Therefore, the equation for center-to-center distance was used:
 
 $$𝐶={{𝑑_{𝑝}+𝑑_{𝑐}} \over 2}=𝑟_{𝑝}+𝑟_{𝑐} $$
 
 $$ 𝑚= {𝑑 \over 𝑁} $$
 
 $$ 𝐶_{1}=𝐶_{2}=𝑚_{1}(𝑁_{𝑝1}+𝑁_{𝑐1})= 𝑚_{2}(𝑁_{𝑝2}+𝑁_{𝑐2}) $$
 
 Proceeding with the equation, it was observed that the distances between centers did not match (difference of a few millimeters between the gear pairs), making it necessary to change the initial value of 16 teeth for the first gear. A value that fit the calculations was 18 teeth (for gear 1). Thus, the values for the number of teeth of the other gears were established:
 
<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198156108-8d21bb5c-8236-4490-b767-fe766f4f5598.png" width=20% height=20%>
</p>
<p align="center">
Tab. 3 - Number of gear teeth
</p>

Based on the range of values generally used for gear width according to Juvinall (2013, p. 341), 9𝑚<𝑏<14𝑚, for the minimum we defined:
 
<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198156282-2aed8452-e8dd-45ca-b1da-31a60edbd16a.png" width=20% height=20%>
</p>
<p align="center">
Tab. 4.1 - Gear width
</p>

However, at the conclusion of the gear strength verification process (discussed later) it was realized that the dimensions could be smaller for gears 1, 2, 3, and 4, and that gears 5 and 6 needed a larger width. Therefore, arbitrarily and based on the resistances, the widths were defined as widths were defined as:

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198156415-be1fb366-2330-4d26-abfb-2b291c19e5c8.png" width=20% height=20%>
</p>
<p align="center">
Tab. 4.2 - Gear width
</p>

For the material, the cheapest of the steels available in the tables was chosen available in the book by Juvinall (2013, p. 459), with the following properties:

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198156835-f80352ea-18b4-49e7-af16-8508299d217e.png" width=50% height=50%>
</p>
<p align="center">
Tab. 5 - Gear material
</p>

Then the calculations of the resistances of each gear were performed. The equations used were:

- Bending stress on the gear teeth:

$$𝜎 = {𝐹_{𝑡} \over 𝑚𝑏𝐽} 𝐾_{𝑣}𝐾_{𝑜}𝐾_{𝑚}$$

- Fatigue strength limit:

$$ 𝑆𝑛 = 𝑆𝑛^{′}𝐶_{𝐿}𝐶_{𝐺}𝐶_{𝑠}𝐾_{𝑟}𝐾_{𝑡}𝐾_{𝑚𝑠}$$

- Surface bending stress:

$$ 𝜎_{𝐻} = 𝐶_{𝑝} \sqrt{ {𝐹_{𝑡} \over 𝑏 𝑑_{𝑝} 𝐼} 𝐾_{𝑣} 𝐾_{𝑜} 𝐾_{𝑚}} $$

- Resistance to surface fatigue:

$$ 𝑆_{𝐻}= 𝑆_{𝑓𝑒} 𝐶_{𝐿𝑖} 𝐶_{𝑅} $$


The values, factors used, and results have been organized in the table below:

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198158027-84906a99-7450-40be-8d34-db69b44bb7c7.png" width=50% height=50%>
</p>
<p align="center">
Tab. 6 - Gear sizing
</p>

Note: The design factor used was 1.5. And the estimated life is $10^{7}$ cycles.
The graphs and tables from which the factors were extracted are in Appendix B.

It was noticed that the surface fatigue resistance was extremely high compared to the required surface strength. No measures were taken to correct these values, since a less hard material would require changes in geometries due to the lower tensile strength, as in the case of aluminum alloys.

With all the strengths appropriately higher than required, the gear design could be completed.

### SHAFT DESIGN

To start, the axial arrangement of the elements in the shaft needed to be defined in order to obtain the acting bending moments and then dimension the required diameters. In this step several iterations were necessary, because the distances had to be changed during the process.

Ftool[^2] software was used to assist in the bending moment and tilt/deflection calculations (needed later in bearing design). Bending moment diagrams are available in Appendix A.

[^2]: https://www.ftool.com.br/Ftool - A Graphical-Interactive Program for Teaching Structural Behavior.

To investigate the necessary strength at each point of interest of the shafts, and define the minimum required diameter, Goodman's Deflection Energy criterion was used, whose equations used were:

- Resistência à fadiga:

$$ 𝑆𝑛= 𝑆𝑛^{′}𝐶_{𝐿} 𝐶_{𝐺} 𝐶_{𝑆} 𝐶_{𝑇} 𝐶_{𝑅} $$

Note: Factor tables following Juvinall's (2013) criteria were used, as they resulted in a worse condition (lower resistance) compared to Budynas' (2011) references.

- Minimum diameter - DE Goodman according to Budynas (2011, p. 692):

$$ 𝑑= {16𝑛 \over 𝜋} ({ {1 \over 𝑆𝑛} [4(𝐾_{𝑓}𝑀_{𝑎})^{2}+3(𝐾_{𝑓𝑠}𝑇_{𝑎})^{2}]^{1 \over 2} + {1 \over 𝑆_{𝑢𝑡}} [4(𝐾_{𝑓}𝑀_{𝑚})^{2}+3(𝐾_{𝑓𝑠}𝑇_{𝑚})^{2}]^{1 \over 2} })^{1 \over 3} $$

Being:

$$ 𝐾_{𝑓}=1+(𝐾_{𝑡}−1)𝑞

The tables whose factors were used are shown in Appendix B.

Thus, a table was assembled to help visualize the results for each axis, where the figure preceding each one shows the dimensions chosen and the points of interest:

Notes:
- For the sections where the gears would be engaged, the stress concentration factor approximation for keys available in Appendix B was used;
- factor of safety/design used was 1.5 and the lifetime was estimated to be 10^{7} cycles;
- The material used was the same as for the gears:

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198156835-f80352ea-18b4-49e7-af16-8508299d217e.png" width=50% height=50%>
</p>
<p align="center">
Tab. 7 - Shaft material
</p>

- The following figures exemplify the cases that will be cited later later:

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198159362-68cfeb61-8c99-4494-8a7c-e1075902a6c1.png" width=50% height=50%>
</p>
<p align="center">
Fig. 4.1 - Case 0 (neutral gear)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198159394-e1bf2ed4-faa3-4cc2-8fbb-40babc3998ac.png" width=50% height=50%>
</p>
<p align="center">
Fig. 4.2 - Case 1 (first gear)
</p>


<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198159430-5fb7c59c-a02f-491e-bc73-a809d903f696.png" width=50% height=50%>
</p>
<p align="center">
Fig. 4.3 - Case 2 (second gear)
</p>

#### Shaft a

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198159507-4a47344a-ddab-4e51-ad2b-43c8229eb314.png" width=50% height=50%>
</p>
<p align="center">
Fig. 5.1 - Shaft a draft
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198159713-9efe5fe4-d388-47cb-a8f8-37206fd29787.png" width=30% height=30%>
</p>
<p align="center">
Tab. 8 - Shaft a sizing
</p>

#### Shaft b

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198159762-fcda6b0a-6188-481d-a648-adc910310cdc.png" width=70% height=70%>
</p>
<p align="center">
Fig. 5.2 - Shaft b draft
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198160064-0f147596-0959-491c-b8ac-3b408273b53c.png" width=70% height=70%>
</p>
<p align="center">
Tab. 9.1 - Shaft b sizing (case 1)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198160429-7cb2f6b3-cdd7-4360-8e77-854527c5f5fd.png" width=70% height=70%>
</p>
<p align="center">
Tab. 9.2 - Shaft b sizing (case 2)
</p>

#### Shaft c


<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198160532-347ea83a-4d02-46f0-9341-08744b369c12.png" width=70% height=70%>
</p>
<p align="center">
Fig. 5.3 - Shaft c draft
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198160583-c5c5d73a-7136-42f5-904e-1c1c8ea7c2fc.png" width=70% height=70%>
</p>
<p align="center">
Tab. 10.1 - Shaft c sizing (case 1)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198160612-d167da5d-7ec9-4ccf-aa53-bd1c336de71e.png" width=70% height=70%>
</p>
<p align="center">
Tab. 10.2 - Shaft c sizing (case 2)
</p>

The values highlighted in yellow in Tables 10.1 and 10.2 refer to a rough approximation of the stress concentration for a spline section (later discarded and adopted as a plain section - see the chapter on brackets later).

With the minimum required diameters already calculated, the choice of the final values was based on the assembly, in such a way that there were recesses for the fitting of the components to be coupled, trying to leave the middle of the shaft with the largest diameters and the staggering decreasing from there.

Thus, some diameters were much larger than the minimum required. However, the required strength objective was met and the oversizing will serve to reduce shaft deflections.

### BEARING DESIGN

With all the forces acting on the shafts and gears duly calculated, the load capacities of the bearings, for a life consistent with the other gearbox components (10^{7} cycles) could be calculated, according to the following equation:

$$ 𝐶_{r𝑒q}=𝐹_{𝑟}𝐾_{𝑎}({𝐿 \over 𝐾_{𝑟}𝐿_{𝑟} })^{0.3} $$

The tables used to obtain the factors used are available in Appendix B.

The aim was to obtain the simplest possible bearings that could resist the radial forces and support the inclinations of the shafts. Thus, the following table was assembled to help visualization, and the bearings were selected based on the NSK catalog[^3] available at the company's website.

[^3]: https://www.nsk.com.br/upload/file/Cat%C3%A1logo%20Geral%20NSK(1).pdf

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198161135-10593b50-7100-43f2-aff8-7fc8065d2516.png" width=70% height=70%>
</p>
<p align="center">
Tab. 11 - Bearing sizing
</p>

Note: Bearings e1 and e2 refer to the bearings that will couple gears 3 and 5 (of shaft c). And the values highlighted in yellow refer to the maximum values of "r" - corner radius - for bearings e1 and e2.

It is also observed that both deflections and inclinations are quite small and despite not finding the inclination tolerances in the NSK catalog, the deflections are much smaller than the maximum allowed for the class with the smallest tolerance (Class 2: $2.5 \times 10^{-3}$ mm for all diameters used). In addition to falling within the tolerances proposed by Budynas (2011, p. 393) also shown in Figure B17 (Appendix B).

There is no specified diameter limit of the thrust for the bearings in the NSK catalog, except for e1 and e2 which is 58 mm (maximum).

### KEYWAY DESIGN

According to Fig. B18, available in Appendix B, from the shaft diameter the width, size and depth of the groove could be defined. A less resistant material was used (in this case the aluminum alloy 2014-0, with 97 MPa yield strength), with a safety/project factor of 1.2 (not too high because in case of an overload in the system, the key must fail to preserve the other components).

For the key length, the equation for crush strength (worse case than shear strength) was used:

$$ 𝑙= {2𝐹_{𝑛} \over 𝑆_{𝑦}𝑡} $$

Thus, the following table was constructed:

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198161731-703f58d6-19eb-47c5-bbc8-83eb479ae632.png" width=70% height=70%>
</p>
<p align="center">
Tab. 12 - Keyway sizing
</p>

It is worth noting that gears 3 and 5 (both on the c-shaft) are coupled to the shaft through the bearing and there is no need for torque transfer, as this will be through the shifting disk.

Note that the length of the parallel keys (with the exception of gears 3 and 5) is much shorter than the width of the gear concerned.

As a way to add more assembly options, it was decided to calculate the couplings through forced fits. For this, the maximum torque that the adjustment supports had to be calculated, using the following formulas:

$$ 𝑇= { 𝜋𝑓𝑝𝑙𝑑² \over 2} $$

$$ 𝑝= {𝐸𝛿 \over 2𝑑³} [{(d_{0}^{2} - d^{2})(d^{2} - d_{i}^{2}) \over d_{0}^{2} - d_{i}^{2} } ] $$

$$ 𝛿_{𝑚𝑖𝑛}=𝑑_{𝑚𝑖𝑛}−𝐷_{𝑚a𝑥} $$ 

Based on the types of adjustments, as shown in figure B19.1 (available in Appendix B), the following table has been constructed with the values used:

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198162350-21d60f3a-6bd2-43cd-bdb7-02aab6f948dc.png" width=70% height=70%>
</p>
<p align="center">
Tab. 13 - Fitting
</p>

It is worth mentioning that the friction between steels is generally in the range of 0.15<𝑓<0.2. Considering the worst case (lowest friction capacity), 𝑓 = 0.15 was used. And all the adjustments are at the "minimum" required. Decreasing 1 setting level (setting H7/p6) makes the maximum supported torque less than what is needed.

For the disc setting, a splined shaft is ideal, since the H7/u6 setting requires high pressing forces, which makes the assembly process more difficult. The maximum torque capacity for the H7/s6 setting does not support the required torque.

Therefore, you can choose which fastening method to use. And as designers, it is recommended to use the forced fit. In view of the low loads acting on the system. For a more robust case, we would recommend the use of keys to act as a mechanical fuse.

## CAD DESIGN

This chapter will show the CAD models using the student version of the Solid Edge[^4] software as an aid to 3D visualization of the components.

[^4]: Available at: https://solidedge.siemens.com

Technical drawings with quotations and standardized views are available in Appendix C.

### GEARS

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198162735-47df6766-850b-4360-af63-e365baeaae41.png" width=50% height=50%>
</p>
<p align="center">
Fig. G1 - Gear 1
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198163002-990da7f8-eb93-4b09-9b3e-ddcd8fa4e916.png" width=50% height=50%>
</p>
<p align="center">
Fig. G2 - Gear 2
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198163092-d76309d8-e31b-4f12-a684-6a020ce969c4.png" width=50% height=50%>
</p>
<p align="center">
Fig. G3 - Gear 3
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198163148-19a092d6-f312-4dcb-bb3b-b2d95681fb7a.png" width=50% height=50%>
</p>
<p align="center">
Fig. G4 - Gear 4
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198163190-4a02c3c1-917d-4fcd-b89b-f14a2bac8796.png" width=50% height=50%>
</p>
<p align="center">
Fig. G5 - Gear 5
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198163228-747a11b8-b957-48a6-919e-b732a427de35.png" width=50% height=50%>
</p>
<p align="center">
Fig. G6 - Gear 6
</p>

### SHAFTS

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198163300-873c7316-ac9e-47bc-84ba-7d38c21ba9e5.png" width=50% height=50%>
</p>
<p align="center">
Fig. S1 - Shaft a
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198163328-9b784d95-8e72-493b-8636-c289a342efd0.png" width=50% height=50%>
</p>
<p align="center">
Fig. S2 - Shaft b
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198163365-292d4df6-69d6-422f-830a-461b5c1ff2e5.png" width=50% height=50%>
</p>
<p align="center">
Fig. S3 - Shaft c
</p>

### BEARINGS

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198163464-9d8ce5d5-77e4-404e-abe6-be38002ed1b2.png" width=50% height=50%>
</p>
<p align="center">
Fig. M1 - Ball Bearing 20 mm
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198163500-c6e32149-a1e6-4f58-bad3-3e94c7ff5196.png" width=50% height=50%>
</p>
<p align="center">
Fig. M2 - Ball Bearing 25 mm
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198163557-de26f187-88c3-416a-9b2d-8e6d64b16740.png" width=50% height=50%>
</p>
<p align="center">
Fig. M3 - Ball Bearing 35 mm
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198163573-71e4ba49-0a2c-4af7-9c8d-b57693dd5495.png" width=50% height=50%>
</p>
<p align="center">
Fig. M4 - Roller Bearing 40 mm
</p>

### SHIFT SYSTEM

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198163691-397d27f4-83f1-4326-a5cb-e0360aa9f80e.png" width=50% height=50%>
</p>
<p align="center">
Fig. V1 - Disc Coupler
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198163725-e54ddca5-7b2a-4006-b9f0-b8112d114d36.png" width=50% height=50%>
</p>
<p align="center">
Fig. V2 - Disc
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198163761-076fda85-c251-439c-9b90-bc4a1281fbd4.png" width=50% height=50%>
</p>
<p align="center">
Fig. V3.1 - Mechanism
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198163815-b763e32d-0520-400d-b4c4-c3c7aa8e5dac.png" width=50% height=50%>
</p>
<p align="center">
Fig. V3.2 - Mechanism
</p>

### BOX

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198163952-9e8d876d-2ac8-4633-9925-993d87d5fe6f.png" width=50% height=50%>
</p>
<p align="center">
Fig. C1.1 - Body
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198163966-819ff317-8fff-4e8b-aca2-3658d464f230.png" width=50% height=50%>
</p>
<p align="center">
Fig. C1.2 - Body
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198164030-4c3effd7-f626-4458-8f03-97d3f4d32c35.png" width=50% height=50%>
</p>
<p align="center">
Fig. C2 - Cover
</p>

### ASSEMBLY

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198164092-e1cdc3ec-f17b-49a1-918a-f831a2197ea4.png" width=50% height=50%>
</p>
<p align="center">
Fig. P1.1 - Gearbox
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198164144-22809bf2-8d82-47f9-bfe4-fa918da8ff7d.png" width=50% height=50%>
</p>
<p align="center">
Fig. P1.2 - Gearbox
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198164176-cf47d7e2-4e96-400b-a11a-2552b10bc55e.png" width=90% height=90%>
</p>
<p align="center">
Fig. P2 - Rendered cut Gearbox
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198164241-2f9cd4ff-4c1c-478a-bbc2-8a12fd39aa46.png" width=90% height=90%>
</p>
<p align="center">
Fig. P3 - Exploded view
</p>

## CONCLUSION

Because it is an "open" project, several decisions could have been different, such as the gear ratios, component material, shaft dimensions, bearing designs, and attachment methods for this same application. Knowing this in advance, the focus of the development was to size the elements as simply as possible with the smallest geometry, cheapest material, with easy manufacturing and assembly.

The gear strength calculations showed that it would be possible to choose a material with lower tensile strength and hardness. However, AISI 1015 facilitates forced fit coupling and requires smaller dimensions to support the loads.

Some designed shaft diameters could be smaller, but the localized stress concentrations in the cross-section differences would be high and the stepped profile would have more abrupt changes (due to some required diameters being high, close to the ones chosen).

The bearings were selected basically following the inner diameter restriction, since the radial load capacity of the selected bearings was not a critical factor, as the acting forces were not that high.

The forced fit coupling was a decision based on the simplicity of making the shafts (for not requiring settlements) and for reducing the number of elements in the transmission set. Despite having a slightly more complicated assembly than keys, as the system does not require constant adjustments, the assembly factor had a lower weight, finalizing the decision for the forced adjustment.

We have succeeded in designing a compact gearbox, made of relatively inexpensive steel, that reliably withstands the loads required for the application, without fatigue failure for the given lifetime, and provides reasonable torques and speeds.

About the project in general, the process of iteration at each stage of the made the work more stressful, but it reinforced the engineering techniques learned in class and reduced the chances of error in the results through the various checks.

## REFERENCES

JUVINALL, Robert. Fundamentos do Projeto de Componentes de Máquinas. 4ª ed. LTC, 2008.

BUDYNAS, Richard. Elementos de Máquinas de Shigley: Projeto de Engenharia Mecânica. 8ª ed. AMGH, 2011.

Wolfram Alpha Computational Inteligence. Wolfram Alpha. Available at: https://www.wolframalpha.com. Access: june 15 2021.

NSK Motion & Control. NSK Rolamentos. Available at: https://www.nsk.com.br. Access: june 29 2021.

## APENDIX A - BENDING MOMENT DIAGRAMS IN FTOOL

Note: For shafts "a" and "c" the views in Ftool were built from the values of the resultant force, since it wouldn't matter the direction of the force, since it is the only one acting on the axis. Differently, the "b" shaft is with separate views.

### SHAFT a

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198164705-03d1800b-ee3f-42a8-a5d9-be6dacebca89.png" width=50% height=50%>
</p>
<p align="center">
Fig. A.1 - Bending moment diagram shaft a
</p>

### SHAFT b

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198164762-bbc255ea-eb71-4ee2-8140-ccf5bef9ef70.png" width=50% height=50%>
</p>
<p align="center">
Fig. A.2.1 - Bending moment diagram b axis (case 1 for the xy plane)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198164805-5a7abe1c-a793-4d45-9ada-916b12e2651a.png" width=50% height=50%>
</p>
<p align="center">
Fig. A.2.2 - Bending moment diagram b axis (case 1 for the xz plane)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198164898-3f051453-961a-4ab0-97de-4524b4225b3a.png" width=50% height=50%>
</p>
<p align="center">
Fig. A.2.3 - Bending moment diagram b axis (case 2 for the xy plane)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198164943-8f86a27e-1892-4dac-b472-765ed4f6329c.png" width=50% height=50%>
</p>
<p align="center">
Fig. A.2.4 - Bending moment diagram b axis (case 2 for the xz plane)
</p>

### SHAFT c

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198165025-81364b6e-fa92-4641-88d5-13aca1037c38.png" width=50% height=50%>
</p>
<p align="center">
Fig. A.3.1 - Bending moment diagram c axis (case 1)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198165065-04d7a2ef-5a39-4158-b20f-f18cb0015713.png" width=50% height=50%>
</p>
<p align="center">
Fig. A.3.2 - Bending moment diagram c axis (case 2)
</p>

## APENDIX B - GRAPHS AND TABLE FOR THE FACTORS USED

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198165225-603cdad4-d667-4949-9b9d-b189a2675bf5.png" width=50% height=50%>
</p>
<p align="center">
Fig. B1 - Geometry factor (J) for Φ = 20°; Source: Juvinall (2013, p. 350)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198165313-d2ac22c1-855a-41d9-8638-fd9b660f12af.png" width=50% height=50%>
</p>
<p align="center">
Fig. B2 - Speed factor Kv (used C curve); Source: Juvinall (2013, p. 350)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198165379-2d9e8362-5fa6-4117-abcc-5d1466ea0e5c.png" width=50% height=50%>
</p>
<p align="center">
Fig. B3 - Overload factor Ko; Source: Juvinall (2013, p. 351)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198165407-dcc94ade-be45-4227-921f-fdd3a622d5d6.png" width=50% height=50%>
</p>
<p align="center">
Fig. B4 - Assembly factor Km; Source: Juvinall (2013, p. 351)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198165504-ce9010a6-4e30-4f40-85e7-d8c33fa300a3.png" width=50% height=50%>
</p>
<p align="center">
Fig. B5 - Surface factor Cs; Source: Juvinall (2013, p. 168)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198165618-4f3504cb-eb3d-4c39-bc3b-b5e557c9e3e8.png" width=50% height=50%>
</p>
<p align="center">
Fig. B6 - Resistance factors (CL, CG, CT and CR); Source: Juvinall (2013, p. 169)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198165690-03786496-c77d-4f8e-b755-7687c54d83ce.png" width=50% height=50%>
</p>
<p align="center">
Fig. B7 - Reliability factor Kr; Source: Juvinall (2013, p. 351)
</p>

For $K_{t}$ and $K_{ms}$, according to Juvinall (2013, p. 351), $𝐾_{𝑡}=1$ if $𝑇<160 °𝐹$ and $𝐾_{𝑚𝑠}=1.4$ for gears with bending in only 1 direction.

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198165789-55039a80-8b9d-4f57-9dfe-c9a77920dcf8.png" width=50% height=50%>
</p>
<p align="center">
Fig. B8 - Elastic coefficient Cp; Source: Juvinall (2013, p. 354)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198165896-7e7cfc5d-6ec7-4276-801f-3a327b402ace.png" width=50% height=50%>
</p>
<p align="center">
Fig. B9 - Surface fatigue strength $S_{fe}$; Source: Juvinall (2013, p. 355)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198165969-47ffa7d4-0cc2-495e-9058-8a80e1369083.png" width=50% height=50%>
</p>
<p align="center">
Fig. B10 - Life factor with respect to surface fatigue $C_{Li}$; Source: Juvinall (2013, p. 355)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198166040-b755a7ab-af05-4aab-8e59-506c31411f62.png" width=50% height=50%>
</p>
<p align="center">
Fig. B11 - Reliability Factor $C_{r}$; Source: Juvinall (2013, p. 355)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198166124-389ba221-68b5-4744-9551-07c4353b548a.png" width=50% height=50%>
</p>
<p align="center">
Fig. B12 - Stress Concentration Factor $K_{t}$ (approximations for fillets and seats); Source: Budynas (2011, p. 387)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198166228-31847817-e0f5-4467-b7c5-dcc557ce9ab8.png" width=50% height=50%>
</p>
<p align="center">
Fig. B13 - Notch sensitivity factor $q$; Source: Juvinall (2013, p. 176)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198166331-9bec146a-b6a7-4aa3-b4e5-8fa9d1674f39.png" width=50% height=50%>
</p>
<p align="center">
Fig. B14.1 - Stress concentration factor (for bending moment); Source: Juvinall (2013, p. 149)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198166384-6b808468-42c8-40b6-8ad0-01337a976b68.png" width=50% height=50%>
</p>
<p align="center">
Fig. B14.2 - Stress concentration factor (for torsion); Source: Juvinall (2013, p. 149)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198166470-05306596-a96a-4542-9701-696c651dcb1b.png" width=50% height=50%>
</p>
<p align="center">
Fig. B15 - Reliability factor (for rolling element bearings); Source: Juvinall (2013, p. 553)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198166534-c1984ee7-4b58-4f35-b1fa-5fcc07d722a7.png" width=50% height=50%>
</p>
<p align="center">
Fig. B16 - Pinning factor (for rolling bearings); Source: Juvinall (2013, p. 554)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198166596-503a047f-e440-4e4e-965d-63939b7c0380.png" width=50% height=50%>
</p>
<p align="center">
Fig. B17 - Slope and transverse deflection tolerances; Source: Budynas (2011, p. 393)
</p>

<p align="center">
<img src="hhttps://user-images.githubusercontent.com/44821460/198166661-586b64e4-d6ba-4395-b61a-b48e5e127e4f.png" width=50% height=50%>
</p>
<p align="center">
Fig. B18 - Dimensions for Keyways; Source: Budynas (2011, p. 405)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198166683-7830dcbe-b364-4d17-a4ce-07abac9c3c9f.png" width=50% height=50%>
</p>
<p align="center">
Fig. B19.1 - Description of Preferred Settings; Source: Budynas (2011, p. 411)
</p>


<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198166818-6a696bb0-2624-4829-bfa5-83e6a483708e.png" width=50% height=50%>
</p>
<p align="center">
Fig. B19.2 - Tolerance class; Source: Budynas (2011, p. 1026)
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/44821460/198166957-9ccd6162-fb9a-4eb6-a073-c65f9ed58b22.png" width=50% height=50%>
</p>
<p align="center">
Fig. B19.3 - Fundamental axis shifts; Source: Budynas (2011, p. 1027)
</p>

## TECHNICAL PLOTS

[Technical Plots](https://github.com/flaviohasd/Mechanical-Projects/files/9874843/Pranchas.pdf)

## EXCEL FILE

[Excel File](https://github.com/flaviohasd/Mechanical-Projects/files/9874857/Projeto.-.Caixa.de.transmissao.xlsx)

## ORIGINAL PAPERWORK (IN PORTUGUESE)

[Caixa de Transmissão.pdf](https://github.com/flaviohasd/Mechanical-Projects/files/9874903/Caixa.de.Transmissao.pdf)


