Disclaimer:

    This research was conducted exclusively in a controlled ArduPilot SITL simulation environment for academic purposes. 
    No physical drones or live RF transmissions were involved. This repository is intended for educational and research purposes only. 
    Any real-world application of these techniques requires proper legal authorization.

HI! This is a project I did over the course of a summer and presented!

The research was used to demonstrate an authentication vulnerability in the MAVLink 2 communication protocol used by ArduPilot powered drones.

CVE Reference:

    CVE-2020-10282

Some context for the project:

    ArduPilot is an open source autopilot operating system widely used in hobbyist and commercial drone platforms. 
    It communicates using MAVLink 2, a lightweight protocol that includes optional packet signing for authentication. 
    However, signing is disabled by default and even when it is enabled the protocol will accept commands that are running on MAVLink 1. 
    What this means is that theoretically a third party actor could with the right equipment to establish themselves as a secondary ground control connection could connect mid-flight and issue commands without authentication,
    resulting in a forced controlled landing or whatever other commands they craft.

Environment:

    ArduPilot SITL — Software In The Loop simulation,
    Python 3.14.4,
    pymavlink 2.4.49,
    MAVProxy 1.8.74,
    ArduPilot V4.8.0-dev,
    WSL2 Ubuntu on Windows

