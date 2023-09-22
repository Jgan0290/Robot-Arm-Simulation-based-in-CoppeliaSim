# Overview
This project implements a simulation of robotic nuclear fuel rod handling using the CoppeliaSim/V-REP software. The goal is to demonstrate the process of robotically picking up nuclear fuel rods, passing them between robots, and accurately placing them into receptacles.
The simulation utilizes four Niryo-1 robotic arms to complete the fuel rod handling task. Two scenarios were developed: a laboratory scene to test basic functionalities, and a factory scene to test continuous operation.

# Robot Implementation
- Niryo-1 robots with 6 degrees of freedom were used as the manipulators
- Forward kinematics implemented to control robot joint angles
- Proximity sensors added to robots to detect fuel rods and trigger motions
- Communication between robots via signals to coordinate fuel rod passing

# Scenes and Features
Laboratory Scene
<p>
  ![Lab Scene](https://github.com/Jgan0290/Robotic-Arm-Fuel-Rod-Handling-Simulation/assets/72658054/2e38c1c9-242f-4c78-bd1e-f2950087a20e)
</p>
- Four Niryo robots passing fuel rod through perspex wall holes
- Sensors on wall holes to detect fuel rod and signal next robot
- Receptacle with sensors to detect open slots for fuel rod placement
Factory Scene
<p>
  ![Factory Scene](https://github.com/Jgan0290/Robotic-Arm-Fuel-Rod-Handling-Simulation/assets/72658054/4d0ca3d4-9219-4c97-bf6f-39753de1793f)
</p>
- Conveyor belt continually feeds fuel rods to first robot
- Robots work continuously to pass rods and fill receptacle slots
- Sensors stop belt when rod in position and detect open receptacle slots

# Results
- Robots successfully passed fuel rod between each other in the lab scene
- Issues encountered in factory scene:
  - Fuel rods falling off conveyor belt due to high speeds
  - Unsynchronized robot motions interfering with passing
  - Inaccurate placement in receptacle slots
- Solved by:
  - Reducing conveyor belt speed
  - Increasing spacing between fuel rods
  - Increasing robot joint velocities/accelerations

# Conclusion
The project demonstrated robotic coordination via sensors and signaling to complete a nuclear fuel rod handling task. Some limitations were uncovered in the continuous factory setting related to robot positioning and conveyance. These could be addressed in future work by implementing inverse kinematics for more precise robot motions and adding collision avoidance capabilities.
