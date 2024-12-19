# SR-FLIPFLOP-USING-CASE

**AIM:**

To implement  SR flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

SR Flip-Flop SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/0f710028-ad52-4d3e-9276-8714cf023a25)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dabfc4f4-87e3-4cbc-9472-f89ee1b5ed30)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dd90d16c-aec5-4290-a586-e2346b1e9eb5)

 
By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/473efad6-d70b-4ca7-aeb7-898bbfca319f)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

**Procedure**

 1. Type the program in Quartus software.
 2. Compile and run the program.
 3. Generate the RTL schematic and save the logic diagram
 4. Create nodes for inputs and outputs to generate the timing diagram.
 5. For different input combinations generate the timing diagram

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by:PRIYADHARSHINI J
RegisterNumber:24901116
 Program for flipflops and verify its truth table in quartus using Verilog programming.
 module sr_flipflop (
 input clk,    // Clock signal
 input reset,  // Active-high reset signal
 input s,      // Set input
 input r,      // Reset input
 output reg q, // Output
 output reg q_bar // Complement of output);
 always @(posedge clk or posedge reset) begin
    if (reset) begin
    
        q <= 1'b0;      // Reset the flip-flop
        
        q_bar <= 1'b1;  // Complement output
    end
    
    
    else begin
    
        case ({s, r})
        
            2'b00: ;             // No change
            
            2'b01: begin         // Reset
            
                q <= 1'b0;
                
                q_bar <= 1'b1;
            end
            
            
            2'b10: begin         // Set
            
                q <= 1'b1;
                
                q_bar <= 1'b0;

                 end
                 2'b11: begin    // I
*/

**RTL LOGIC FOR FLIPFLOPS**
![Screenshot 2024-12-19 062050](https://github.com/user-attachments/assets/cbdeda2f-a39b-44d0-a93e-46b0b0e63f11)


**TIMING DIGRAMS FOR FLIP FLOPS**
![Screenshot 2024-12-19 062112](https://github.com/user-attachments/assets/5d76d25f-772f-42e5-80ec-0d5ba2e0395f)

**RESULTS**
```
 Thus the SR flipflop using verilog is implemented and validated their functionality using
 their functional tables
```
