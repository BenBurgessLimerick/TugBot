# TugBot
The TugBot mobile robotics development platform was designed around two objectives:
1. Learn how to develop robots in the ROS ecosystem
2. Develop a system to assist in towing small boats up and down from a lake

These two objectives provide the constraints for the design of the system. In particular, the second objective is fleshed out into the following problem specification:
- Distance between house and lake: 500m
- Mass of boats: 50-200kg
- Speed required: walking speed, 0-5 km/h
- Terrain capabilities: Road surfaces, hill between lake and house

## TugBot Design
The TugBot is a 4 wheel drive skid steer platform. Propulsion is achieved by repurposed HoverBoard wheels controlled by ODrive brushless motor drivers. The HoverBoard wheels provide an integrated motor and wheel assembly with position feedback given by a Hall effect encoder. The wheels are easy to mount by clamping the fixed shaft onto the robot’s chassis. The ODrive motor controllers allow for a digital interface to the precise control of brushless motors. A guide for controlling a HoverBoard wheel with an ODrive controller can be found [here](https://github.com/madcowswe/ODrive/blob/master/docs/hoverboard.md).
Unfortunately, the ODrive does not yet have a well supported C++ ROS driver, so a basic driver was developed: [odrive_cpp_ros](link).

## ROS Packages
The skid steer design of the TugBot is similar to the design of Clearpath’s [Husky](link). The Husky is also developed on the ROS platform and provided the perfect starting point to begin the journey of learning ROS, and deploying it on a custom developed platform. Most of the ROS packages below are adapted from packages designed for the Husky.
