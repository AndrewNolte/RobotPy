# RobotPy

This repo is a fork of of the original [Robotpy](http://robotpy.github.io) , which is a pure python implementation of WPILIB, used in First Robotics Competitions.

This version strips all of the FRC specific stuff out, including hardware and network tables.

It adds on the fly customizable commands, via triggers and assists.

It replaces the Networktables frontend with a Flask Server.

It allows for easy simulation support via a hardware abstraction layer that can be set up with AirSim.

## Control Protocol

There are two frameworks natively supported and customary to robotpy. One is a state machine paradigm, which uses functions
and state returns to transfer control. Essentially command switching is determines by the child process currently executing, rather than the parent process that
invoked that command. This can be somewhat overwhelming for large programs, but more simplistic for smaller ones.

The reccomended approach is command-based, where individual commands are defined with init, execute, end, etc. These can easily be combined with triggers and assists for
easy code reuse. Then those commands can be added to command groups, for a simple high level definition of multiple complex children processes, which can be combined in parallel or sequential groups.
