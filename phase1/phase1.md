## **Executive Summary**

A six speed manual transmission is a mechanical system that is designed to transfer power from the engine to the drive wheels of a vehicle. The driver then has the option to select from multiple gear ratios to optimize the drivability of the vehicle in many different scenarios on the road. Key advantages of using such a system is improved fuel usage, wider range of gear ratios, and a more enhanced driving experience. This specific mechanical system operates through the use of multiple combinations of gears, shafts, and synchronizers which in turn creates a robust and efficient drivetrain solution. This report will explain many different concepts of the six gear manual transmission system, going from how the general system works, key components, and some potential failure points in such a system.

![](https://github.com/RyanT2004/MEE342-Group-9/blob/main/images/GIF.gif)

## **System Function and Decomposition**
A manual transmission system works in tandem with the engine and flywheel. Power from the engine enters the transmission through the input shaft and then passes through the selected gear ratio. The multiple gear ratios in the transmission system determines the speed and torque one would want in a situation. That power then exits the system using the output shaft which is connected to the drivetrain of the vehicle.

In order to ensure smooth gear transitioning and engagement, synchronizers are used in order to match rotational speeds before the meshing of the gear teeth which also reduces wear on the gears as well. The clutch in the system serves as a way to easily shift between gears and does so by temporarily disconnecting engine power when shifting.

![](https://github.com/RyanT2004/MEE342-Group-9/blob/main/images/Diagram.jpg)

## **Parts List**

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

**Possible Failures:**  
Misalignment: A misalignment occurs when the shafts bends under high gear loading forces. This causes the gear teeth to mesh at an angle instead of perfectly parallel which leads to uneven stress distribution across the tooth face and premature gear pitting.  

Excessive Torque on Output Shaft: In most 6 gear transmissions, having too much torque applied to the output shaft can cause possible angle of twist on the shaft which would wear out the shaft faster.

Forks on Shift Rods have potential to break: Ensure that material is able to handle the force caused by the synchronizer without snapping.

Wear on Gears over time: In practice and on a full scale a lubricant would be added in order to help the gears longevity 

Gears Seize / Grinding Gears: Calculate gear ratios as well as making sure the rotational direction is aligned, we also need to check the distance between gears in order to make sure there is no accidental motion between gears.

Possible Structural Deflection due to Heavy Gears on Shafts: Check kinematics of the shaft and check material shear stress.

**Possible Solutions to These Issues:**  
To address most of these issues, we will test multiple iterations of the transmission via different gear ratios and different sizes of critical components to find the perfect balance that will mitigate these failures.

## **Transmission Diagram**
![](https://github.com/RyanT2004/MEE342-Group-9/blob/main/images/Manual%20Transmission%20System.png)

## **Critical Components**

Components where design purposes are especially important:
* **Gears:** Finding the right gear ratios will be the main task to focus on as each gear setting in the transmission will determine a vehicle’s speed output and torque.
* **Input/Output Shafts:** Determining the diameter of the input and output shaft will ensure that the transmission can switch between gears easier and to make sure the shafts can support the weight of all the gears without it snapping under the weight.
* **Housing:** The housing must fit the entire system with as little spare room as possible to save material and to make sure the system does not move too much.
* **Synchronizers:** Synchronizers will work with the different gear ratios to help make shifting into a different gear smoother and more efficient. Both the gears and synchronizer will need to have proper dimensions so that each will not get in each other's way.

![](https://github.com/RyanT2004/MEE342-Group-9/blob/main/images/Synchronizer.png)

## **Critical Design Parameters**
* 5 forward gears + 1 reverse gear
* PETG material will be used to model transmission
* Gear tooth and ratios

  1st: Input 20T, Output 50 T = 2.5:1  
  2nd: Input 28T, Output 42 T = 1.5:1  
  3rd: Input 32T, Output 38 T = 1.19:1  
  4th: Input 34T, Output 36 T = 1.06:1  
  5th: Input 35T, Output 35 T = 1:1  
  6th: Input 38T, Output 32 T = 0.84:1

* Input/Output Shaft Diameter 25.4 mm
* Clearances TBD
* Distance between gears TBD
* Distance between input/output Shaft TBD
  
## **References**
https://californiamotorsports.net/pages/porsche-901-transaxle-specification  
https://www.artofmanliness.com/skills/manly-know-how/gearhead-101-understanding-manual-transmission/  
