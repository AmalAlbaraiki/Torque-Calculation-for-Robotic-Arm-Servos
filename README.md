Report on Calculating the Required Torque for Servo Motors in the Robot Arm
Introduction:
This report outlines the calculations for the required torque for each servo motor in the robot arm. The torque is determined based on the given weights and dimensions of different parts of the arm, including movable parts such as joints and the gripper. The purpose of these calculations is to ensure the selection of motors that can handle the required loads and ensure optimal performance of the robot.
Given Data:
•	Gravity: 9.81 m/s²
•	Weight of the object to be carried: 1 kg
•	Length of parts:
o	Part 1: 15 cm (0.15 m)
o	Part 2: 10 cm (0.10 m)
o	Gripper: 4 cm (0.04 m)
•	Arm weight: 0.3 kg for each part (assumed) for part 1 and part 2
•	Gripper weight: 0.2 kg
Calculation Method:
The following equations were used to calculate the required torque:
1.	Torque = Force × Distance
o	Force (F): weight × gravity
o	Distance: distance from the axis of rotation to the center of mass (joint to center of mass of the arm or gripper).
2.	The torque at joint 1 (T1), joint 2 (T2), and joint 3 (T3) was calculated as follows:
o	Torque at joint 1:
T1=(Fload×(L1+L2))+(Fgripper×(L1+L2−L3/2))+(Farm2×(L1+L2/2))+(Farm1×(L1/2))T1 = (F_{\text{load}} \times (L1 + L2)) + (F_{\text{gripper}} \times (L1 + L2 - L3/2)) + (F_{\text{arm2}} \times (L1 + L2/2)) + (F_{\text{arm1}} \times (L1/2))T1=(Fload×(L1+L2))+(Fgripper×(L1+L2−L3/2))+(Farm2×(L1+L2/2))+(Farm1×(L1/2))
o	Torque at joint 2:
T2=(Fload×L2)+(Fgripper×(L2−L3/2))+(Farm2×(L2/2))T2 = (F_{\text{load}} \times L2) + (F_{\text{gripper}} \times (L2 - L3/2)) + (F_{\text{arm2}} \times (L2/2))T2=(Fload×L2)+(Fgripper×(L2−L3/2))+(Farm2×(L2/2))
o	Torque at the gripper:
T3=Fload×(L3/2)T3 = F_{\text{load}} \times (L3/2)T3=Fload×(L3/2)
Calculation Results:
The required torques for the different joints were calculated as follows:
•	Torque at joint 1 (T1): 3.71 N·m
•	Torque at joint 2 (T2): 1.29 N·m
•	Torque at the gripper (T3): 0.20 N·m
Selecting the Suitable Servo Motors:
1.	Joint 1 (T1):
o	The required motor should support a torque of at least 5.57 N·m.
o	Suggested motor:
2.	Robodo MG996R TowerPro MG996R Servo Motor : Buy Online at Best Price in KSA - Souq is now Amazon.sa: ToysJoint 2 (T2):
o	The required motor should support a torque of at least 1.94 N·m.
o	Suggested motor:
3.	Deegoo-FPV 4PCS Servo Motor MG995 Control Angle180 Metal Gear Servo 20KG Digital High Speed Torque Servo Motor for Smart Car Robot Boat RC Helicopter : Buy Online at Best Price in KSA - Souq is now Amazon.sa: Toys
4.	Joint 3 (T3):
o	The required motor should support a torque of at least 0.30 N·m.
o	Suggested motor:

	OWOOTECC 20KG Servo Motor DS3218 (~2.2 N·m)
https://www.amazon.sa/-/en/owootecc-Torque-Digital-Waterproof-Control/dp/B0819LWL9V
Torque Calculation Code :
 calculate the torque for each motor based on the given data:
python
# Given data
g = 9.81  # Gravity (m/s^2)
m_load = 1  # Load weight (kg)
l1 = 0.15  # Length of part 1 (m)
l2 = 0.10  # Length of part 2 (m)
l3 = 0.04  # Length of gripper (m)

# Calculating load force
F_load = m_load * g

# Assuming arm weights are around 0.3 kg for each part
m_arm1 = 0.3  # Weight of part 1 (kg)
m_arm2 = 0.3  # Weight of part 2 (kg)
m_gripper = 0.2  # Weight of gripper (kg)

# Calculating part forces
F_arm1 = m_arm1 * g
F_arm2 = m_arm2 * g
F_gripper = m_gripper * g

# Calculating torque at joint 1 (base)
T1 = (F_load * (l1 + l2)) + (F_gripper * (l1 + l2 - l3/2)) + (F_arm2 * (l1 + l2/2)) + (F_arm1 * (l1/2))

# Calculating torque at joint 2
T2 = (F_load * l2) + (F_gripper * (l2 - l3/2)) + (F_arm2 * (l2/2))

# Calculating torque at the gripper
T3 = F_load * l3 / 2

T1, T2, T3  # Printing results
This code was included in the GitHub repository for easy access and implementation.
Conclusion:
The required torques were accurately calculated, and the appropriate motors were selected based on these calculations to ensure optimal performance of the robot. The necessary links to purchase the motors were also included, along with the code used for the calculations.
________________________________________
Notes:
•	The safety margin was considered to ensure the motors operate optimally.
•	The servo motors were selected based on the calculated torques with an additional safety margin.
________________________________________

