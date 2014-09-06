#System Architecture#

##Processing Distribution##

###"One Ring"###

A single uC doing everything, Flight Control, Motor Control and Comms

###Twins###

One uC for the motors, one uC for the rest.

###Typical###

One control uC and an additional uC per motor.

###Madness###

One uC per function
- Comms
- Flight
- Sensors
- Motor A
- Motor B
- ...

##Inter-Processor-Comms##

###I2C###
###SPI###
###UART###
###PWM###