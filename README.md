## Austins Modified Ardupilot

Welcome to my modified ArduPilot repository for improving the flight capabilities of larger Group 2 UAS.

All of the following file changes are made to those in the ArduPlane folder as this work focuses on fixed-wing vehicles.

## SIM_Plane.h

Use SIM_Plane_h_vals.csv

* hover_throttle (line XX)
* CGOffset (line XX)
* Aircraft parameters (lines XX - XX)

## SIM_Frame.h

Use SIM_Frame_vals.csv

* refVoltage (line XX)
* maxVoltage (line width)
* battCapacityAh (line XX)
* hoverThrOut (line X)
* disc_area (line XX)
* mass (line X)
* propExpo (line XX)

## SIM_Plane.cpp

Use SIM_Plane_cpp_vals.csv

* mass (line XX)

## Group2.parm

Run this file in the SITL console after running
```
> cd ArduPlane
> sim_vehicle.py -j4 -v Plane -f quadplane --console
```

Currently this file does not need to be informed by a CSV. When aircraft configurations (quadplane, tiltrotor, tailsitter, v-tail, etc.) are implemented, this file will need to be made informable via CSV.

* param set SIM_BATT_VOLTAGE 50
* param set Q_RTL_MODE 1
* param set RTL_RADIUS 300
* param set ARSPD_FBW_MIN 18
* param set ARSPD_FBW_MAX 50
* param set Q_ANGLE_MAX 3000
* param set Q_M_THST_EXPO 0.75
