## EIE2 Instruction Set Architecture & Compiler (IAC)

---
## Lab 2 - Signal Generation and Capture


### Task 1

Python file generates sine wave outputs and creates the file **_sinegen.mem_** 

**_counter.sv_** has a new input "incr"

### Task 2
Added a new input "off" to represent offset, that is controlled by Vbdvalue().
This is the input to rom.sv and there is an additional output "dout2". 
ROM now has an additional input and 2 outputs (dout and dout2), where dout2 is the original wave with the offset.
