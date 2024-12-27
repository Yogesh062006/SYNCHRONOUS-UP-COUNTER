### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**

/* write all the steps invloved */
1.Write the detailed procedure here.
2.Type the program in Quartus software.
3.Compile and run the program.
4.Generate the RTL schematic and save the logic diagram.
5.Create nodes for inputs and outputs to generate the timing diagram.
6.For different input combinations generate the timing diagram.


**PROGRAM**
```
/* Program for flipflops and verify its truth table in quartus using Verilog programming.
UP COUNTER
module ex11(out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(rst)
     out<=0;
   else 
     out <= out+1;
end
endmodule
```

Developed by:S Yogesh
RegisterNumber:24901108


**RTL**
![image](https://github.com/user-attachments/assets/b32027cb-444e-4fc9-ac68-817f98287483)

**TRUTH TABLE**
![image](https://github.com/user-attachments/assets/538ef975-fa8c-4874-ac9c-0032ca5c7aad)

**OUTPUTS**
![image](https://github.com/user-attachments/assets/50d6b7e6-5494-41c4-a8b1-b0038433e2c5)

**RESULTS**
4-bit synchoronous up counter is verified. 
