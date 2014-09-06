#Software Architecture#


##Single VS Multi Threaded##


##Polled VS Interrupt Driven##


##Flight Model / Control Mechanisms##

###Multi-Model VS Single Model###

- Do we model control inputs as disturbances?

###*Plugable Flight Control!*###

####IFlightControl####

##Languages##

- C
- C++
  - GCC
  - Clang
  - Other
- D
  - LDC
  - GDC
  - Std Library not yet really in place for bare metal.
    - oportunity to contribute
    - distraction from the project.
- ADA
  
[effh: My preference is C++, this is not the project to start playing with D]
  
##RTOS##

- FreeRTOS
- ecos
- QNX
- ThreadX
- vxWorks