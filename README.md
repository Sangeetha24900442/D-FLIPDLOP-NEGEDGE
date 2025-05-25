# D-FLIPDLOP-NEGEDGE

**AIM:**

To implement  D flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/48c81fe8-bc3f-40e7-95e2-519fc155ad51)

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/e5f3fda7-68ec-4a3a-a0a4-cf6f9cc4ab55)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

**Procedure**

/* write all the steps invloved */

1.Write the Verilog code for a D flip-flop that triggers on the negative edge of the clock and includes an active-low reset.

2.Use an always @ (negedge Clock) block to describe flip-flop behavior.

3.Inside the block, check if reset is low (!reset) to asynchronously clear Q to 0.

4.If reset is high, assign the input D to output Q using non-blocking assignment (<=).

5.Simulate the design using a testbench to verify reset and data capture functionality.



**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 
Developed by: SANGEETHA S
RegisterNumber:212224040287

```
module exp8(D,Clock,reset,Q);
input D,reset,Clock;
output reg Q;
always @ (negedge Clock)
if(!reset)
Q <= 0;
else
Q <= D;
endmodule
```
*/

**RTL LOGIC FOR FLIPFLOPS**

![Screenshot 2025-05-25 153858](https://github.com/user-attachments/assets/4dd7d511-079d-4a8d-9a0e-5e90b063111b)



**TIMING DIGRAMS FOR FLIP FLOPS**

![Screenshot 2025-05-25 154135](https://github.com/user-attachments/assets/908a9839-d669-4bc6-8151-0de6900d6f19)



**RESULTS**
Thus the program is verified and executed successfully.
