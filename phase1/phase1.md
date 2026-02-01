## **Parts List With Definitions**

**Input shaft**  
The input shaft is the power-entry component that transmits torque from the engine into the gearbox. It is typically splined to the clutch disc and carries the initial drive gear that meshes with the countershaft. It also serves as a pilot support for the output shaft, requiring a high degree of concentricity to prevent vibration and ensure smooth power transfer to the rest of the gear train.

**Counter shaft (Gear assembly)**  
The counter shaft is the component that carries a series of fixed gears of varying diameters that rotate together to provide multiple reduction stages for the output gears. It serves as the intermediate power path, receiving torque from the input shaft and distributing it to the various “free” gears on the output shaft. 

**Output shaft (Gear assembly)**  
The output shaft is the last component in the system of the transmission. It transmits torque and rotation to the load. The output shaft receives motion from the gear train, transmits the motion outward to the wheels, and provides the adjusted speed and torque that the gears were designed to produce.

**Gears (1st - 6th, and reverse), helical and straight cut gears**  
Manage power output to the wheels by deciding the torque applied to the output shaft.

**Synchronizers (hub, sleeve, blocker ring)**  
The synchronizers are engaged by the forks of the shift fork which is connected to the shift rod and gear shift.  

**Shift forks**  
Moves the synchronizer sleeves to engage specific gears in order to determine the gear we are in.

**Reverse Idler gear**  
This component reverses the output shaft in order for the vehicle to have reverse capabilities.

**Bearings**  
The bearings minimize the friction between moving parts. 

**Gear shift (sub-assembly)**  
Shift lever and rods connecting the shift forks/synchronizer sleeves to the driver, controls which gears are engaged. 

## **Kinematic Breakdown – 6 Gear Transmission**

**Motion Path (Power Flow)**  
Power enters the system through the input shaft and is transferred to the countershaft through an input gear mesh. From the countershaft, power is transmitted through one selected gear pair to the output shaft, which delivers motion to the load.

Input shaft → Input gear → Countershaft → Selected gear pair → Output shaft

**Direction of Rotation**  
The transmission uses a three-shaft (layshaft) configuration with two gear meshes in the forward power path. The first gear mesh between the input shaft and countershaft reverses the direction of rotation. The second gear mesh between the countershaft and output shaft reverses the direction again.

Result: The output shaft rotates in the same direction as the input shaft.

**Gear Ratio**  
The gear ratio determines the relationship between input speed and output speed and controls torque multiplication.

N<sub>I</sub>​ = number of teeth on the input gear  
N<sub>C0</sub> = number of teeth on the countershaft gear meshing with the input  
N<sub>Ck</sub>​ = number of teeth on the selected countershaft gear  
N<sub>Ok​</sub> = number of teeth on the matching output gear

The total gear ratio for gear k is:  
### $R_k=\frac{N_{C0}}{N_I} * \frac{N_{Ok}}{N_{Ck}}$


A larger gear ratio provides higher torque and lower output speed (lower gears), while a smaller gear ratio provides lower torque and higher output speed (higher gears).

**Key States / Positions**  
Neutral: No gear is engaged with the output shaft; input and countershaft may rotate without driving the output.

1st Gear: Highest gear ratio; maximum torque and lowest output speed.
2nd Gear
3rd Gear
4th Gear
5th Gear
6th Gear: Lowest gear ratio; minimum torque and highest output speed.

Only one gear is engaged at a time. Shifting occurs by disengaging the current gear and engaging the next gear in sequence.

## **Preliminary Failure Mode Review**

**Possible Failures**  
Misalignment: A misalignment occurs when the shafts bends under high gear loading forces. This causes the gear teeth to mesh at an angle instead of perfectly parallel which leads to uneven stress distribution across the tooth face and premature gear pitting.  

Excessive Torque on Output Shaft: In most 6 gear transmissions, having too much torque applied to the output shaft can cause possible angle of twist on the shaft which would wear out the shaft faster.

Forks on Shift Rods have potential to break: Ensure that material is able to handle the force caused by the synchronizer without snapping.

Wear on Gears over time: In practice and on a full scale a lubricant would be added in order to help the gears longevity 

Gears Seize / Grinding Gears: Calculate gear ratios as well as making sure the rotational direction is aligned, we also need to check the distance between gears in order to make sure there is no accidental motion between gears.

Possible Structural Deflection due to Heavy Gears on Shafts: Check kinematics of the shaft and check material shear stress.

**Possible Solutions to These Issues**  
To address most of these issues, we will test multiple iterations of the transmission via different gear ratios and different sizes of critical components to find the perfect balance that will mitigate these failures.

## **Transmission Diagram**


## **Critical Components**

Components where design purposes are especially important:
* Gears
* Input/Output Shafts
* Housing
* Synchronizers

## **Critical Design Parameters**
* 5 forward gears + 1 reverse gear
* PETG material will be used to model transmission
* Gear tooth and ratios TBD
* Shaft Diameter TBD
* Clearances TBD
* Distance between gears TBD
* Distance between input/output Shaft TBD
