## **Final Design Overview**
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

(Clear assumptions and results from all analyses performed)

Static Stress and Factor of Safety

Fatigue Assessment

Gear Tooth Loading

Interface Stresses

Bearing Load Check

Global Safety Overview

---
## **Design For Assembly and 3D Printing Discussion**

<div align="center">

  
| Parts | Images |
|:----------|:--------|
| **Shaft Ring** |  <img src="../images/ShaftRing.PNG" width="600"> |
| **Shaft** |  <img src="../images/Shaft.PNG" width="600"> |
| **Synchronizer** |  <img src="../images/synchro.PNG" width="600"> |
| **Synchronizer Coupler** |  <img src="../images/SynchroCoupler.PNG" width="600"> |
| **Shifter** |  <img src="../images/Shifter.PNG" width="600"> |
| **Shift Box** |  <img src="../images/ShiftBox.PNG" width="600"> |
| **Housing** |  <img src="../images/Housing_Test.PNG" width="600"> |
| **Mesh Gears** |  <img src="../images/GearMesh.PNG" width="600"> |
| **Gear Coupler** |  <img src="../images/GearCoupler.PNG" width="600"> |
| **Fork Coupler** |  <img src="../images/Fork_Coupler.PNG" width="600"> |
| **Shift Cradler Shaft** |  <img src="../images/Shift_Cradle_Generic.PNG" width="600"> |
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
The transmission model created is similar to the real world designs with a few adjustments due to some lack of knowledge and materials. Despite that, the system will act as an actual transmission with all key components designed and optimized for our half-model. While building the model, the biggest concern was the distance between all the components, especially the gear pairs. Having improper distancing can lead to a multitude of design failures, the one that was most concerning was possible seizing of gears. This would create unintended motions between the gears which could possibly affect the rotational direction. The solution that was used was to mitigate this as well as other possible system failures was to test multiple iterations of the transmission. These iterations would have different gear ratios and critical design components in order to find the perfect balance between all of the parts. These dimensions would also be used to calculate different engineering analysis which would also help determine the final dimensions used in the transmission. After finalizing every part, all that was left was to design them in SolidWorks and put it all together in an assembly build to visualize the final product. The most efficient method of combining all the parts of the system together was to create smaller subs assemblies of the system and then adding those assemblies into the final full assembly. This was done for the synchronizer, input shaft, and output shaft. These components were selected as the sub assemblies since they were the main complex components that could prove to be an issue if done improperly. Doing these in parts will mitigate any problems when it comes to mating all our parts since we could easily figure out where a problem could occur and troubleshoot. The final design after compiling all the components shows the intended motion and idea of how a manual transmission would work.

**3D Printing Design Discussion:**  
While creating all the parts in SolidWorks, we were already accounting for how the parts could be printed when it was time to create the physical model. Each part was specifically designed so that the printer would have no issues printing out each part taking into account how a 3D printer works. There is also the chance that the part created will be slightly smaller than the dimensions listed in the print file which also proved to not be an issue due to the error range that was determined when looking through the dimensions. The only part that could have been an issue was the housing to hold all the critical components since it was significantly bigger than the size of the printer area. The solution to this was to split the housing into two sections and print each section out individually. The two sections can then be combined using any binding agent and it will then be used to store everything.

---

## **Anticipated Risks & Weaknesses in Prototyping**

Some anticipated risks that could be seen when prototyping is:
* Shrinkage of 3D parts after printing could affect fit.
* Improper sizing of parts that were accidentally overlooked when creating parts.
* Structural failure specifically in the shafts of the transmission.

