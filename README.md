# JKFLIPFLOP-USING-IF-ELSE
**EXP7: JK FLIPFLOP**

NAME:VIJAYAKUMAR.S

REG NO.24900562


**AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**JK Flip-Flop**

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/a649c30b-232b-4558-b188-fd6c09845180)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/c4360742-e8a8-4937-b089-c46c0433f9a3)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/6c275261-a6d5-4c37-a3a7-1e88ca11c4cd)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/5174f41b-0ce0-4329-a372-6d1943ea6673)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

**Procedure**

1. Type the program in Quartus software.

2. Compile and run the program.

3. Generate the RTL schematic and save the logic diagram.

4. Create nodes for inputs and outputs to generate the timing diagram.

5. For different input combinations generate the timing diagram.



**PROGRAM**

Program for flipflops and verify its truth table in quartus using Verilog programming. 

module jkv(q,qbar,clk,j,k);

input j,k,clk;

output q,qbar;

wire nand1_out; 

wire nand2_out; 

nand(nand1_out, j,clk,qbar);

nand(nand2_out, k,clk,q);

nand(q,qbar,nand1_out);

nand(qbar,q,nand2_out);

endmodule 


**RTL LOGIC FOR FLIPFLOPS**

![Screenshot 2024-12-04 082649](https://github.com/user-attachments/assets/8f24109d-abfa-48d4-bd47-bdc50dc4d8ab)

**TIMING DIGRAMS FOR FLIP FLOPS**

![Screenshot 2024-12-04 082908](https://github.com/user-attachments/assets/091ee42e-ebc8-4fba-a8d9-7374a2466738)

**RESULTS**
 Thus JK flipflop using verilog is implemented and their functionality using their functional tables is validated.
