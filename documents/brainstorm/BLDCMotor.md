#BLDC Motor Control#
##Shoot Through Limitation##
Repeated for each phase of each motor.
Hi = H in
Ho = L out etc
Hi|Li|Ho|Lo|Valid|Hi.Valid|Li.Valid
--|--|--|--|-----|--------|--------
 0| 0| 0| 0|    1|       0|       0
 0| 1| 0| 1|    1|       0|       1
 1| 0| 1| 0|    1|       1|       0
 1| 1| 0| 0|    0|       0|       0
Valid = NAND(Hi, Lo)
Ho = AND(Valid, Hi)
Lo = AND(Valid, Lo)
###Possible implimentations###
-Discrete
-Small CPLD
-Small Memory Device
##Drive Pattern##
H = +ve L = Ground Z = high impeadence
State|Phase A | Phase B | Phase C
-----|--------|---------|--------
    0|       H|        L|       Z
    1|       H|        Z|       L
    2|       Z|        H|       L
    3|       L|        H|       Z
    4|       L|        Z|       H
    5|       Z|        L|       H
    0|       H|        L|       Z
From ST AN1946.
##Starting##
-Soft Start
-Jerk Start
-Feedback?
##Sensors VS Sensorless##
##Open Loop VS closed loop##
Do we actually need to go closed loop?
##Current Limiting##
Resistance Based
PWM chopping
**Must** modulate Hi to prevent charge pump collapse.
###Current Sensing Mechanism###
Synchronise ADC reads to H-On phases of PWM signal.
##Transistors##
###Protective Diodes###