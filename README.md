## Austins Modified Ardupilot

This repository is a modified version of ArduPilot for enabling the SITL flight and simulation of Group 2 UAS.

## SIM_Plane.h

Found in ``` ardupilot\libraries\SITL ```

Inform using SIM_Plane_h_vals.csv from ``` ardupilot\ArduPlane\csv_mods ```

* hover_throttle (line 43)
* Aircraft parameters (lines 52 - 89)
* CGOffset (line 92)

## SIM_Frame.h

Found in ``` ardupilot\libraries\SITL ```

Inform using SIM_Frame_vals.csv from ``` ardupilot\ArduPlane\csv_mods ```

* mass (line 84)
* diagonal_size (line 87)
* refVoltage (line 94)
* refCurrent (line 95)
* maxVoltage (line 101)
* battCapacityAh (line 104)
* hoverThrOut (line 107)
* propExpo (line 110)
* disc_area (line 130)

## SIM_Plane.cpp

Found in ``` ardupilot\libraries\SITL ```

Inform using SIM_Plane_cpp_vals.csv from ``` ardupilot\ArduPlane\csv_mods ```

* mass (line 31)

## Group2.parm

Found in ``` ardupilot\Tools\autotest\default_params ```

Run this file in the SITL console after running
```
> cd ardupilot/ArduPlane
> sim_vehicle.py -j4 -v Plane -f quadplane --console
> param load ../Tools/autotest/default_params/Group2.parm
```

Currently this file does not need to be informed by a CSV. When aircraft configurations (quadplane, tiltrotor, tailsitter, v-tail, etc.) are implemented, this file will need to be made informable via CSV.

* param set Q_ENABLE 1
* param set SIM_BATT_VOLTAGE 50
* param set Q_RTL_MODE 1
* param set RTL_RADIUS 300
* param set ARSPD_FBW_MIN 18
* param set ARSPD_FBW_MAX 50
* param set Q_ANGLE_MAX 3000
* param set Q_M_THST_EXPO 0.75
