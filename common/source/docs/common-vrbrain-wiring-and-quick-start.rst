.. _common-vrbrain-wiring-and-quick-start:

==========================
Vrbrain Wiring Quick Start
==========================

This article provides high level information about how to power your VrBrain and connect its most important peripherals.
Only the latest revisions will be covered on this page. If you own an older version or need more advanced specific information, it can be found on the vrbrain wordpress: <https://vrbrain.wordpress.com/>


VrBrain 5 Wiring Chart
======================



Powering the board
===================



Connecting remote control inputs
================================

Pixhawk is compatible with 
   #. PPM remote control (R/C) receivers
   #. Futaba S.Bus receivers

For traditional single-wire-per-channel (PWM) receivers a PPM encoder
can be used to convert the receiver outputs to PPM-SUM. 

.. tip::

   Information about compatible receivers and how they are connected can be found in :ref:`Compatible RC Transmitter and Receiver Systems (Pixhawk/PX4) <common-pixhawk-and-px4-compatible-rc-transmitter-and-receiver-systems>`.

.. figure:: ../../../images/FRSkyTaranis.jpg
   :target: ../_images/FRSkyTaranis.jpg

   FRSky Taranis Transmitter

Connecting a buzzer
====================

The buzzer and safety switch button are mandatory for Pixhawk. Connect
to the BUZZER and SWITCH ports as shown.

.. image:: ../../../images/pixhawk-required_peripherals.jpg
    :target: ../_images/pixhawk-required_peripherals.jpg

.. warning::

   Mount the beeper at least 5cm away from the flight
   controller or the noise may upset the accelerometers.

GPS/Compass Module
==================

The :ref:`3DR UBlox GPS + Compass Module <common-installing-3dr-ublox-gps-compass-module>` is the
recommended GPS for Pixhawk on ArduPilot.  The GPS ports are connected
with the six-position DF13 cable, and the MAG port is connected to the
I2C port with the four-position DF13 cable.

.. figure:: ../../../images/GPS_TopAndSide.jpg
   :target: ../_images/GPS_TopAndSide.jpg

   3DR UBlox GPS + Compass Module

The topic :ref:`3DR UBlox GPS + Compass Module <common-installing-3dr-ublox-gps-compass-module_connecting_to_pixhawk>`
shows how to connect to Pixhawk and include additional configuration and
mounting information.

Connect Motors
==============

.. image:: ../../../images/pixhawk_motor_outputs.jpg
    :target: ../_images/pixhawk_motor_outputs.jpg

[site wiki="copter"]
For Copter see :ref:`Connect ESCs and Motors <copter:connect-escs-and-motors>`.

In overview, for copters connect each signal wire from the PDB to the
main output signal (S) pins by motor number:

-  Pin 1 = Motor 1 - - Pin 5 = Motor 5
-  Pin 2 = Motor 2 - - Pin 6 = Motor 6
-  Pin 3 = Motor 3 - - Pin 7 = Motor 7
-  Pin 4 = Motor 4 - - Pin 8 = Motor 8

[/site]

[site wiki="plane"]
For planes connect the control channel wires to the main output signal
pins:

-  Pin 1 = Aileron
-  Pin 2 = Elevator
-  Pin 3 = Throttle
-  Pin 4 = Rudder

[/site]

[site wiki="rover"]
For Rovers connect the throttle and steering wires to the main output
signal pins:

-  Pin 3 = Throttle
-  Pin 1 = Steering

The skid-steer parameters are used to configure vehicles that have fixed wheels and steer like tank tracks (do not use servos to steer the wheels but rather use differential speed between the left and right wheels). The parameters are: SKID_STEER_OUT and SKID_STEER_IN. When enabled, flight controller's ouput RC1 is used for the left track control, and ouput RC3 is used for right track control.
[/site]

Connect other peripherals
=========================

Depending on your hardware there may be any number of other peripherals
attached, including sensors, cameras, grippers etc. These can be found
as sub-pages of the topic :ref:`Optional Hardware <common-optional-hardware>`.

Information about connecting these peripherals to Pixhawk is found in
the respective pages.

Related information
===================
