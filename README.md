# SPIKE_communication
Information what SPIKE uses to communicate


SPIKE Hub sends out a stream with informations

Modes:
======

Standard m:0
------------
{"m":0,"p":[[0, []], [0, []], [0, []], [0, []], [0, []], [0, []], [-9, -4, 988], [-1, 5, 0], [-1, 0, 0], "09090:99999:99999:09990:00900", 0]}}
mode, p_data[PortA[IDofDevice,[Values]],PortB[IDofDevice,[Values]],PortC[IDofDevice,[Values]],PortD[IDofDevice,[Values]],PortE[IDofDevice,[Values]],PortF[IDofDevice,[Values]], Acceleration[],Gyro[],Orientation[],DisplayedImage,ProgramRuntimerINms]

Standard-Output is send out all 48ms

Battery m:2
-----------
{'m': 2, 'p': [8.359999999999999, 100]}
mode, p_data[Volrage,BatteryCharge%]

Button m:3
----------
{"m":3,"p":["center", 170]}]}
mode, p_data[whichButton,durationOfPressedINms]

Values:
- leftside
- center
- rightside



Gestures m:4
------------
{"m":4,"p":"tapped"}

Values:
tapped
doubletapped
shake
Front
Rightside
Leftside
Up
down


Variables m:11
--------------
One Variable:
{'m': 11, 'p': ['JgoemqN7S87hsA55CTRZ', {'mySingle': '9468468361638296365367844'}, {}, {}]}
Two Variable:
{'m': 11, 'p': ['JgoemqN7S87hsA55CTRZ', {'outputSingle': '2139526830186527963198648', 'mySingle': '2139526830186527963198648'}, {}, {}]}
Two Variable and one List:
{'m': 11, 'p': ['JgoemqN7S87hsA55CTRZ', {'outputSingle': '9009203367698688500571251', 'mySingle': '9009203367698688500571251'}, {'allSingles': ['6833521043907758565864567', '3082044060851564630806410', '0331091476786632865496549', '7477258101353361152710961', '3754630264082759521617118', '7526857612387157675709618', '2646705638483885677481293', '4459723760751868459105357', '9009203367698688500571251']}, {}]}


Device Output-Values:
=====================
Used in Standard Mode m:0 ... PortA->PortF
SimpleMotor (WeDo, Boost):
ID,[SpeedValue]

AdvancedMotor (SPIKE):
ID,[ActualSpeed,ChangesofDegrees°,ActualPosition°,ForceToKeepSpeed]

ID:
1 WeDo Motor (10 Steps)
38 Boost Motor (9 Steps)
48 SPIKE middle Motor (Advanced Values)
49 SPIKE Large Motor (Advanced Values)

SpeedValues: -100 <-> 100 (negative: counterclock/positive clockwise)



SUPPORTED Sensors:
==================
Fully Supported:
SPIKE ColorSensor
SPIKE DistanceSensor
SPIKE ForceSensor
WeDo2.0 DistanceSensor
WeDo2.0 Gyro

Partly Supported:
Boost Color/DistanceSensor only ColorSensor


SUPPORTED Motors:
=================
SPIKE MiddleMotor (Advanced)
SPIKE LargeMotor (Advanced)
WeDo2.0 Motor
Boost Motor





















