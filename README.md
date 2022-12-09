# Maze Runner Robot

<p align="center">
  <img src="https://github.com/TuanNguyen4/maze-runner-robot/blob/main/media/maze-runner-robot-1.gif" width="75%">
</p>

## Description
This is one of the projects I worked on when I was an electrical engineering student. For this class, we were tasked with building and programming a maze runner robot. I worked on this with two other people: Ryan Le and Kevin Tieu. 

The build process was divided into ten labs, each focused on a robot function like bluetooth interfacing, configuring distance sensor, setting up motors, and implementing PID control. The brain of the robot is a [TM4C123GXL microcontroller](https://www.ti.com/tool/EK-TM4C123GXL) and the program was developed in C++ using Code Composer Studio IDE. A bluetooth module is used to communicate wirelessly with the robot to start/stop it and receive data while it is traveling in the maze. 

<p align="center">
 <img src="https://github.com/TuanNguyen4/maze-runner-robot/blob/main/media/Robot.jpg" width="40%" >
</p>

The robot's inputs are two IR distance sensors and a reflectance sensor. Both distance sensors are attached to the front with one facing forward and one facing right. The reflectance sensor is pointed at the ground to detect the black, electrical tapes in the maze. The outputs are two DC motors, powered by a dual motor driver carrier. I also designed and 3D printed the platform to hold the breadboard and microcontroller.

<p align="center">
  <img src="https://github.com/TuanNguyen4/maze-runner-robot/blob/main/media/Front%20view.jpg" width="33%" >
  <img src="https://github.com/TuanNguyen4/maze-runner-robot/blob/main/media/Top%20view.jpg" width="33%" >
</p>

## PID Controller
We deployed a right-hand-on-wall method and programmed proportional-integral-derivative (PID) control using the right distance sensor. We defined a set distance for the robot to maintain from the wall and the sensor will continuously update its actual position. Based on the feedback, the robot will adjust the duty cycle of the motors to minimize the steady state error. If the front sensor detects a wall, the robot will stop to perform a U-turn and continue. 

<p align="center">
  <img src="https://github.com/TuanNguyen4/maze-runner-robot/blob/main/media/maze-runner-robot-1.gif" width="45%">
  <img src="https://github.com/TuanNguyen4/maze-runner-robot/blob/main/media/maze-runner-robot-2.gif" width="45%">
</p>

## Wiring Diagram
<p align='center'>
  <img src="https://github.com/TuanNguyen4/maze-runner-robot/blob/main/media/Wiring%20Diagram.jpeg" width="50%" >
</p>
