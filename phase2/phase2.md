## **Final Design Overview & Model Explanation**
---
<div align="center">
  <img src="../images/FULL_ASSEMBLY_WH_ISO_2.PNG">
  <p><em>Figure 1. Isometric View Without Housing.</em></p>
</div>

<div align="center">
  <img src="../images/FULL_ASSEMBLY_WH_ISO.PNG">
  <p><em>Figure 2. Full Model Isometric View.</em></p>
</div>

<div align="center">
  <img src="../images/FULL_ASSEMBLY_WH_SIDE.PNG">
  <p><em>Figure 3. Full Model Side View.</em></p>
</div>

<div align="center">
  <img src="../images/FULL_ASSEMBLY_WH_TOP.PNG">
  <p><em>Figure 4. Full Model Top View.</em></p>
</div>

<br>

In the model created in SolidWorks, the input gear spins the output gear that is fixed to the other shaft, creating the desired output torque. Its important to note that these gears are isolated cases since its not depicted well in SolidWorks due to mating capabilities. How it works is that the synchro locks into the selected gear setting using the gear shifter and the inner ring of the synchro is always moving with the shaft. In the assembly, all gears are free floating on the shaft until its mated to be locked to the synchro using mates and constraints.

---
## **Major Design Decisions & Changes**

**Adjusted gear ratios so that each pair had the same total tooth count (70 tooth total for each pair):**   
The ratios were changed so that it would help with gear meshing in the transmission system while also keeping proper torque and output speeds with each respective gear pair.

**Decreased size of input and output shaft 25.4 mm → 20 mm:**  
After going through a few iterations, the input and output shafts were deemed too thick which would have led to waste of materials when printing and would have affected the power output of the transmission.

**Transmission housing was split into 2 parts:**  
This was done so that the part could actually be printed out using the 3D printers. The plan is to attach both parts together which should cause any issues since it's just the housing that holds everything together.

**Distance between input and output shaft was determined to be 125 mm:**  
This was determined through estimations of calculations and analysis and after finalizing the gear ratio sizes, this was the ideal distance between both shafts.

**Adjusted distance between gear pairs as listed:**
* 1st and 2nd gear 60 mm
* 2nd gear and 3rd gear 5 mm
* 3rd gear and 4th gear 60 mm
* 4th gear to 5th gear 5 mm
* 5th gear to 6th gear 60 mm

This was changed after doing more research on how real world transmission gear pair distances were established. These distances would lower the chances of gears not meshing or possible misalignment in the system.

---
## **Detailed Explanation Of Analyses**

**Static Stress and Factor of Safety**

We performed a static stress analysis focusing on the transmission’s response to a peak input torque of 1500 N.m. Our analysis tracked the torque multiplication across all six gear pairs, reaching a maximum output of 1781.25 N.m in the sixth gear. By applying these loads to our 20 mm shafts, we evaluated the bending and torsional stresses against the material's yield strength. This high-torque scenario represents our primary safety constraint, and the results confirm that the shaft geometry and material selection provide a robust factor of safety, preventing permanent deformation during sudden gear shifts or heavy acceleration.

NGO = number of teeth on output gear  
NGI = number of teeth on input gear  

<!--
eff = efficiency factor (assumed to be 100%)  
T<sub>initial</sub> = initial torque from the input rod (1500 N.m)


<div align="center">
  
Output Torque = T<sub>initial</sub> * $\frac{NGO}{NGI}$ * eff
  
Torque on 1st gear = 1500 * $\frac{20}{50}$ * 1 = 600 N.m

Torque on 2nd gear = 1500 * $\frac{28}{42}$ * 1 = 1000 N.m

Torque on 3rd gear = 1500 * $\frac{32}{38}$ * 1 = 1263 N.m

Torque on 4th gear = 1500 * $\frac{34}{36}$ * 1 = 1416 N.m 

Torque on 5th gear = 1500 * $\frac{35}{35}$ * 1 = 1500 N.m 

Torque on 6th gear = 1500 * $\frac{38}{32}$ * 1 = 1781 N.m
</div>
-->

<div align="center">
  
| Gear Pair | Input Teeth (NGI) | Output Teeth (NGO) | Input Diamter [mm] | Output Diameter [mm] |
|:-------|:-------|:-------|:-------|:-------|
| **Gear 1** | 50 | 20 | 181.78 | 75.71 |
| **Gear 2** | 42 | 28 | 153.49 | 103.99 |
| **Gear 3** | 38 | 32 | 139.35 | 118.14 |
| **Gear 4** | 36 | 34 | 132.28 | 125.21 |
| **Gear 5** | 35 | 35 | 128.74 | 128.74 |
| **Gear 6** | 32 | 38 | 118.14 | 139.35 |
</div>

**Fatigue Assessment**

The fatigue assessment was conducted to ensure the transmission's reliability over its full service life, assuming a standard engine speed of 2000 RPM. Because the input and output shafts rotate under load, they are subject to cyclic stress that can lead to crack initiation. We applied the Modified Goodman Criterion to these components, focusing on the points where the shaft diameter transitions to 20 mm. By confirming that our operating stresses remain well below the endurance limit of the material, we ensure the transmission can withstand millions of cycles without fatigue failure, even at high-speed operation where the pitch line velocity reaches approximately 9948 m/s.

d = pitch diameter (m)  
n = pinion speed (rpm) = 2375  
N = number of teeth of highest gear = 32  
m = module = 2.5 (m)

<div align="center">
  
#### d = m * N = 32 * 2.5 = 80 m

#### V = $\frac{π* d * n}{60}$ = $\frac{π* 80 *2375}{60}$ = 9948 m/s
</div>

**Gear Tooth Loading**

For the gear tooth loading section, we utilized AGMA standards with a focus on the Gear 6 assembly, which handles the highest output torque. The gears were designed with a 2.5 mm module, a 14.5° pressure angle, and a 25 mm face width. We calculated a dynamic factor (Kv) of 1.741 to account for the mesh speeds and quality of the gear teeth. Using these parameters, the AGMA bending stress was calculated to be well within safe limits, indicating that the teeth are sized appropriately to prevent root breakage or surface pitting while maintaining the fixed 125 mm center distance required for the housing.

<div align="center">
  
<img src="../analysis/Calculation Images/AGMA Standards Calculations.png" width="45%"> 
<img src="../analysis/Calculation Images/AGMA Standards Calculations 2.png" width="49%">
<img src="../analysis/Calculation Images/AGMA Geometry Factor for Bending.png" width="49%">
</div>

<br>

**Interface Stresses**

We analyzed the interface stresses at the critical junctions where the gears are keyed to the 20 mm shafts. This analysis involved checking the bearing stress on the key faces and the shear stress across the key cross-sections under the calculated tangential load (Wt). Based on an operating torque of 40.21 N.m used in our test simulations, we verified that the keyways can effectively transmit power without material crushing or shear failure. This ensures a "sacrifice-safe" design, where the key is robust enough for normal operation but protects the more expensive shafts and gears from damage in the event of an extreme mechanical jam.

P = power = 1000 (Watts)  
ω = angular velocity (rad/s)  

<div align="center">
  
#### ω = $\frac{2 * π * n}{60}$ = 248.7 rad/s

#### Operating Torque = $\frac{P}{ω}$ = $\frac{1000}{248.7}$ = 40.31 N.m
</div>

**Bearing Load Check**

The bearing load check was performed to determine the reaction forces generated by the meshing gears. Given the 70-tooth total count for each gear pair and the helical tooth geometry, we calculated the combined radial and axial thrust loads that must be supported by the transmission housing. We compared these loads to the dynamic ratings of our selected bearings to ensure they can maintain shaft alignment during the 2000 RPM operational phase. The results indicate that the bearings are correctly positioned to distribute these loads evenly, preventing shaft deflection that could lead to gear misalignment or housing wear.

**Global Safety Overview**

In conclusion, the Shift Happens transmission design successfully balances high performance with structural safety. By integrating a 6-speed gear range with ratios from 0.4 to 1.1875, we achieved the necessary output torque of 1781.25 N.m while maintaining a compact form factor. Every component, from the 2.5 mm module gears to the optimized 20 mm shafts, was verified through both analytical AGMA formulas and fatigue assessments. This multi-layered analysis confirms that the final assembly is not only capable of meeting the project's torque requirements but is also durable enough for long-term functional use in a prototype environment.

eff = efficiency factor (assumed to be 100%)  
T<sub>initial</sub> = initial torque from the input rod (1500 N.m)  

<div align="center">
  
#### **Output Torque = T<sub>initial</sub> * $\frac{NGO}{NGI}$ * eff**

<br>
 
| Gear Pair | Ratio (G) | Output Torque [N*m] |
|:-------|:-------|:-------|
| **Gear 1** |  0.4 | 600 |
| **Gear 2** |  0.667| 1000 |
| **Gear 3** |  0.8421 | 1263.16 |
| **Gear 4** |  0.9444 | 1416.67 |
| **Gear 5** |  1.0 | 1500 |
| **Gear 6** |  1.1875 | 1781.25 |
</div>

<br>

> These are NOT all of our calculations, the rest is located in the analysis folder. The calculations given here gives an idea of what we parts we solved for and how each part relates to another variable of the whole transmission system analysis.

---
## **Design For Assembly and 3D Printing Discussion**

<div align="center">

  
| Parts | Images | Part Drawing |
|:-------|:-------|:-------|
| **Shaft Ring** |  <img src="../images/ShaftRing.PNG" width="600"> | <img src="../images/Transmission Part Drawings PNG/ShaftRing_Drawing.png" width="700"> |
| **Shaft** |  <img src="../images/Shaft.PNG" width="600"> | <img src="../images/Transmission Part Drawings PNG/Shaft_Drawing.png" width="700"> |
| **Synchronizer** |  <img src="../images/synchro.PNG" width="600"> | <img src="../images/Transmission Part Drawings PNG/synchro_Drawing.png" width="700"> |
| **Synchronizer Coupler** |  <img src="../images/SynchroCoupler.PNG" width="600"> | <img src="../images/Transmission Part Drawings PNG/SynchroCoupler_Drawing.png" width="700"> |
| **Shifter** |  <img src="../images/Shifter.PNG" width="600"> | <img src="../images/Transmission Part Drawings PNG/Shifter_Drawing.png" width="700"> |
| **Shift Box** |  <img src="../images/ShiftBox.PNG" width="600"> | <img src="../images/Transmission Part Drawings PNG/ShiftBox_Drawing.png" width="700"> |
| **Housing** |  <img src="../images/Housing_Test.PNG" width="600"> | <img src="../images/Transmission Part Drawings PNG/Housing Drawing.png" width="700"> |
| **Mesh Gears** |  <img src="../images/GearMesh.PNG" width="600"> | <img src="../images/Transmission Part Drawings PNG/gearMesh_Drawing.png" width="700"> |
| **Gear Coupler** |  <img src="../images/GearCoupler.PNG" width="600"> | <img src="../images/Transmission Part Drawings PNG/GearCoupler_Drawing.png" width="700"> |
| **Fork Coupler** |  <img src="../images/Fork_Coupler.PNG" width="600"> |<img src="../images/Transmission Part Drawings PNG/Fork_Coupler_Drawing.png" width="700"> |
| **Shift Cradler Shaft** |  <img src="../images/Shift_Cradle_Generic.PNG" width="600"> | <img src="../images/Transmission Part Drawings PNG/Shaft_Cradle_Generic_Drawing.png" width="700"> |
| **Input Helical Gears** |  <img src="../images/6th_Input_Updated.PNG" width="600"> | 
| **Output Helical Gears** |  <img src="../images/6th_Updated_Output.PNG" width="600"> | 
  
</div>

> The 6th gear pair were used for the input and output gear images above, but each gear pair for each speed is a different tooth count and size. The image above only gives a reference as to what each one look like as all look very similar to the image given.

From the part list above, separate assemblies were made before all were combined to create the full transmission model. This method allowed us to integrate each component of the system more efficiently with less room for problems as well. Below are the documentation of the assemblies made that were then used in the full model design.

***

Parts Used in Full Synchronizer Assembly:
* 1x Synchronizer
* 2x Gear Couplers

<div align="center">
  <img src="../images/FullSynchro_ISO.PNG">
  <p><em>Figure 5. Synchronizer Assembly.</em></p>
</div>

***

Parts & Assemblies Used in Output Shaft Assembly
* 1x Shaft
* 2x Synchronizer Couplers
* 2x Full Synchronizer Assembly
* 10x Shaft Rings
* 4x Mesh Gears
* 6x Output Helical Gears
* 2x Fork Couplers

<div align="center">
  <img src="../images/FULL_ASSEMBLY_WH_OUTPUT_ASSEMBLY.PNG">
  <p><em>Figure 6. Output Shaft Assembly.</em></p>
</div>

***

Parts/Assemblies Used in Input Shaft Assembly:
* 11x Shaft Rings
* 6x Input Helical Gears
* 1x Shaft
* 2x Mesh Gears
* 1x Fork Coupler
* 1x Full Synchronizer Assembly
* 1x Synchronizer Coupler

<div align="center">
  <img src="../images/FULL_ASSEMBLY_WH_INPUT_ASSEMBLY.PNG">
  <p><em>Figure 7. Input Shaft Assembly.</em></p>
</div>

***
**Assembly Design Discussion:**  
The transmission model created is similar to the real world designs with a few adjustments due to some lack of knowledge and materials. Despite that, the system will act as an actual transmission with all key components designed and optimized for our half-model. While building the model, the biggest concern was the distance between all the components, especially the gear pairs. Having improper distancing can lead to a multitude of design failures, the one that was most concerning was possible seizing of gears. This would create unintended motions between the gears which could possibly affect the rotational direction. The solution that was used was to mitigate this as well as other possible system failures was to test multiple iterations of the transmission. These iterations would have different gear ratios and critical design components in order to find the perfect balance between all of the parts. These dimensions would also be used to calculate different engineering analysis which would also help determine the final dimensions used in the transmission.  
  
After finalizing every part, all that was left was to design them in SolidWorks and put it all together in an assembly build to visualize the final product. The most efficient method of combining all the parts of the system together was to create smaller subs assemblies of the system and then adding those assemblies into the final full assembly. This was done for the synchronizer, input shaft, and output shaft. These components were selected as the sub assemblies since they were the main complex components that could prove to be an issue if done improperly. Doing these in parts will mitigate any problems when it comes to mating all our parts since we could easily figure out where a problem could occur and troubleshoot. The final design after compiling all the components shows the intended motion and idea of how a manual transmission would work.

<div align="center">
  <img src="../images/ExplodedView.gif">
  <p><em>Figure 8. Transmission Exploded View.</em></p>
</div>

**3D Printing Design Discussion:**  
While creating all the parts in SolidWorks, we were already accounting for how the parts could be printed when it was time to create the physical model. Each part was specifically designed so that the printer would have no issues printing out each part taking into account how a 3D printer works. There is also the chance that the part created will be slightly smaller than the dimensions listed in the print file which also proved to not be an issue due to the error range that was determined when looking through the dimensions. The only part that could have been an issue was the housing to hold all the critical components since it was significantly bigger than the size of the printer area. The solution to this was to split the housing into two sections and print each section out individually. The two sections can then be combined using any binding agent and it will then be used to store everything.

---

## **Anticipated Risks & Weaknesses in Prototyping**

Some anticipated risks that could be seen when prototyping is:
* **Shrinkage of 3D parts after printing could affect fit:**
  - This happens with most 3D printing materials, shouldn't affect the final product but important to keep in mind.
* **Improper sizing of parts that were accidentally overlooked when creating parts:**
  - With many different parts being created, some parts could have been made with the wrong dimensions so double checking each part before printing can save a lot of time and material.
* **Structural failure specifically in the shafts of the transmission:**
  - After doing the calculations and running some analyses, it was determined that structure should be able to with stand the stresses and torque applied to it but when it comes time to assemble the parts for the prototype, it could be a different story.

---

## **References**
* Brain, Marshall. “How Gear Ratios Work.” HowStuffWorks, 20 Oct. 2023, science.howstuffworks.com/transport/engines-equipment/gear-ratio.htm. 

* CarTechBooks. “Manual Transmissions Explained.” CarTechBooks, 26 May 2015, www.cartechbooks.com/blogs/techtips/manual-transmissions-explained.   

* Hufford, Kelly. “How Manual Transmission Are Manufactured and Tested.” Transpartswarehouse.com, Transparts Warehouse Inc, 30 Apr. 2024, transpartswarehouse.com/blog/post/how-manual-transmission-are-manufactured-and-tested.
* https://gearsolutions.com/features/determination-of-the-agma-j-factor-for-internal-spur-gears/
* https://www.engineersedge.com/calculators/agma_gear_tooth_bending_stress_15856.htm
