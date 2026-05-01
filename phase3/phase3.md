# **Fabrication Details**

* Printer (Bambu Lab A1) :
    * Plate Temperature: 70 ℃
    * Filament Type: PETG & PLA
    * Volumetric Flow Rate: 18 [mm<sup>3</sup>/s]
    * Flow Ratio: 0.94
    * Density: 1.28 [g/cm<sup>3</sup>]
    * Nozzle Temperature : 230 ℃
* Reprint Count: 
    * 8 reprints on gears and actuators, only 4 reprints were done based on fitting
* Shafts:
    * 6063 Aluminum 

# **Assembly Procedure and Challenges**

For the housing, the front and back were printed out as the entire housing would have used too much filament and would have taken alot much time. PLA was used as it would have resulted in a faster print compared to PETG. Then the hole cutouts for the input and output shafts were drilled, as well as the holes for the forks. All the pieces were then screwed together and the rod and gear assembly were placed inside the housing with the synchronizers. Once we ensured the proper fit was achieved, the forks were put in place and then we tested the assembly to check that everything was functioning properly.

## Step 1: Printing

<div align="center">
  <img src="../images/Step 1.JPG" width="50%">
  <p><em>Figure 1. Printing Out All Components
</div>

## Step 2: Sanding Down Shafts

<div align="center">
  <img src="../images/Step 2.JPG" width="60%">
  <p><em>Figure 2. Sanding Down Input & Output Shafts
</div>

## Step 3: Measuring Distance of All Components

<div align="center">
  <img src="../images/Step 3.JPG" width="60%">
  <p><em>Figure 3. Taking Measurements & Dimensions
</div>

## Step 4: Verifying Components Fits With Shaft

<div align="center">
  <img src="../images/Step 4.jpeg" width="50%">
  <p><em>Figure 4. Gears Being Inserted Into Shaft
</div>

## Step 5: Applying Proper Gears to Input and Output Shaft

<div align="center">
  <img src="../images/Step 5.jpg" width="70%">
  <p><em>Figure 5. Gear Pairs Fully Aligned
</div>

## Step 6: Attach Housing Components and Forks

<div align="center">
  <img src="../images/Step 6.jpg" width="60%">
  <p><em>Figure 6. Final Prototype
</div>

Throughout the process, we encountered several engineering challenges, particularly with dimensional tolerances. Achieving proper fits for bearings and gear teeth required careful adjustment, as even small deviations significantly affected performance. One key issue was material shrinkage. Using the Bambu Lab PETG HF, we observed an average shrinkage of approximately 0.30 mm. To compensate, critical dimensions, especially holes for bearings and interfaces with aluminum tubes, were slightly increased to ensure proper press and slip fits.  

A major issue we encountered was with the aluminum tubes we sourced. Although they were specified with tolerances of ±0.01 mm, the actual measured variation ranged from approximately 0.05 mm to 0.25 mm. This inconsistency significantly impacted bearing fitment, requiring extensive manual sanding of the tubes to achieve the proper diameter. While time-intensive, this step was necessary to ensure smooth rotation and proper assembly of the gear system.  

During assembly, we also observed that some of the gears experienced slight misalignment due to movement caused by adhesive application. Although the gears still engaged and functioned as intended, this introduced minor positioning inconsistencies. In future iterations, this could be improved by implementing a fixture or jig to hold components precisely in place during bonding, ensuring consistent alignment and reducing assembly variability.  

Additionally, the overall scale of the model was larger than initially anticipated, which led to increased material usage and required us to order additional PETG HF filament. The new filament introduced further challenges during printing, including inconsistent extrusion and reduced print reliability. To address this, we adjusted key printing parameters such as bed temperature, nozzle temperature, print speeds, and volumetric flow rates. Through iterative testing and tuning, we were able to restore print quality and ensure consistent results across all components.

# **Test Procedures, Results, and Interpretation**

Despite the challenges, the printing process was ultimately successful. Layer adhesion was strong and consistent, resulting in durable components. For the gears, we optimized the print settings by using a low infill of 10% combined with 6 wall loops. This approach maintained material efficiency while ensuring the gear teeth were solid and capable of handling mechanical loads. The final printed parts achieved a reliable fit and contributed effectively to the functionality of the transmission system. 

**Testing Method**  
The way we tested our prototype was simple. Using the crank handle attached to the input shaft, we spun it to create a torque that would act on the output shaft. As the crank was generating a constant torque, the three forks that were attached to the synchronizers were then shifted separately to lock in each gear pair respectively. We tested this for all 6 gear pairs to ensure each one was meshing properly with no misalignments. The results showed that all 6 modes were successfull and that everything ran smoothly. We also checked that if two pairs were initiated at the same time, the system would lock up and as expected it did. A mini propeller attached to our output shaft was used to gauge the speed and proper movement of each gear set as well. 

Overall, this project strengthened our understanding of additive manufacturing, tolerance control, and material behavior, while also improving our ability to troubleshoot, optimize processes, and adapt under real-world engineering constraints.

# **Failures & Mistakes Discussion**
We ran into many issues with our design during the process of its creation. The first issue we had was with obtaining the shafts for our transmission, as the original size we picked was not available for purchase. To purchase a shaft, we had to round down our shaft size, which significantly altered our stress calculations and ultimately led to a stress condition that failed. To resolve this issue, we had to double our shaft size to ensure it would not fail. Unfortunately, by doubling the diameter of our shaft, the shaft became very expensive, so we had to adjust our shaft to be hollow. This again increased our stress, but it was still lower than the allowable for our material.  

Our second issue was with the helical angle of our helical gears. The default angle SolidWorks created for the gears resulted in excessive bending stress along the shaft, and it was much higher than the angle typically found in a transmission. To fix this, we had to lower the angle to decrease the stress.  

Another one of our errors was with the tolerance of the synchronizers. In our CAD model, they had zero tolerance, so when we printed, the pieces did not fit together. To remedy this, our group added a 0.30 mm tolerance.

Our last major error was with the housing. In creating the design, our group did not recognize that the housing would be too large to print, so we split it into multiple pieces. After deliberation, we then realized that the amount of filament required to print all the pieces of the housing structure would cost too much. To resolve this, we decided to print only the walls of the housing using PLA which would result in a faster and cheaper print.  

After analyzing all of our mistakes, we concluded that with more time spent on research and team communication, many of the failures and mistakes could have been avoided. 

# **Reflection**
**Design Changes from Phase 2:**

* Doubled the shaft size from 20 mm to 40 mm
* Changed helical angle from ~45° to ~15°
* Changed from a solid aluminum shaft to a hollow aluminum shaft.
* Changed the housing from PETG to PLA filament

**Comparison to Phase 2 Predictions**  
In our phase 2 report, we predicted that the transmission might freeze or run into misalignment issues. After conducting our tests, we discovered that neither of these is an issue with our design. We also predicted that the gear teeth of the input and output shafts wouldn't mesh but after finalizing the prototype, the gears were working properly as intended.

**Design Changes for Second Iteration**
* Design a better housing system that doesn't require a lot of material or time to build.
* Expand shaft diameters to eliminate bending and ensure perfect gear teeth alignment.
* Properly adjust CAD dimensions to compensate for filament shrinkage and ensure precise keyway fits.

