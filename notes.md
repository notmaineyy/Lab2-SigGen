## EIE2 Instruction Set Architecture & Compiler (IAC)

---
## Lab 2 - Signal Generation and Capture


### Task 1

Python file generates sine wave outputs and creates the file **_sinegen.mem_** 

**_counter.sv_** has a new input "incr"

### _Test-yourself Challenge_

Modify your design so that you use the **_vbdValue()_** function to chage the frequency of the sinewave generated.

Added 

```C++
    top->incr = vbdValue();
```


### Task 2

Modify your design in Task 1 so that you generate **TWO** simultaenous sinusoid signals which have different phases.  The phase offset between the two sinusoids is determined by the rotary encoder on Vbuddy.  You need to use a dual-port ROM similar to that you used in Task 1. The first port's address **_addr1[7:0]_** is from the counter. The second port's address **_addr2]7:0]_** is offset from the first address.  This offset is read from Vbuddy with the **_vbdValue()_** function.

To display two waveforms on Vbuddy, you can call the **_vbdPlot()_** function twice, first with **_data1[7:0]_**, then with **_data2[7:0]_**.  

#### What was done 
Added a new input "off" to represent offset, that is controlled by Vbdvalue().
This is the input to rom.sv and there is an additional output "dout2". 
ROM now has an additional input and 2 outputs (dout and dout2), where dout2 is the original wave with the offset.

### Task 3
??? does it even work idk