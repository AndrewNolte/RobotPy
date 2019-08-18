# RobotPy

This repo is a fork of of the original [Robotpy](http://robotpy.github.io) , which is a pure python implementation of WPILIB, used in First Robotics Competitions.

This version strips all of the FRC specific stuff out, including hardware and network tables.

It adds on the fly customizable commands, via triggers and assists.

It replaces the Networktables frontend with a Flask Server.

It allows for easy simulation support via a hardware abstraction layer that can be set up with AirSim.
