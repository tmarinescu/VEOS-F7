# VEOS-F7
VEOS alpha (SDOS) for STM32F7


Back when SDOS was called VEOS (Vehicle Embedded Operating System).


It "kind of" works. If the stack is located arbitrarily in RAM it works fine, if it's located in TCMRAM it hard faults several cycles in. 
Something is up with how the RAM is arranged and accessed by the CPU that makes the kernel freak out since TCMRAM is slightly different than CCMRAM which was utilized in the F3/G4.
The manual doesn't bother explaining the inner workings and it's not worth an investigation (after several hours of debugging) right now.
