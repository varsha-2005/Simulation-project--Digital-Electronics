# TITTLE

Design And Simulate Decade Synchronous Upcounter With T FlipFlop Using Verilog

# THEORY

1.A decade synchronous up-counter is a digital circuit that counts sequentially from 0 to 9 and then wraps around back to 0. The "synchronous" part means that the counting operation is synchronized with a clock signal, and the "up" part indicates that the counter increments its value.

2.A T flip-flop is a type of flip-flop that toggles its output (Q) based on the value of its input (T) and the clock signal. When the clock signal transitions from low to high (rising edge or positive edge), the T flip-flop evaluates the input and updates its output accordingly.

3.To implement a decade synchronous up-counter using T flip-flops in Verilog, you can follow these steps:

4.Step 1: Declare the module and its ports:

5.The module is named "decade_counter" and has three ports: clk for the clock signal, reset for resetting the counter, and count as a 4-bit output representing the counter value.

Step 2: Declare internal signals and flip-flops:

6.Here, q is a 4-bit register to store the counter value, and t is the input for the T flip-flop.

Step 3: Instantiate T flip-flops and connect them:

7.In this step, you instantiate four T flip-flops (TFF) and connect them in a chain. Each flip-flop takes the clock signal (clk) and reset signal (reset). The T inputs are connected to the output of the previous flip-flop, forming a ripple carry structure.

Step 4: Define the T inputs based on the counter value:

8.This always block triggers on the positive edge of the clock signal (posedge clk) or the positive edge of the reset signal (posedge reset). Inside the block, the T input is determined based on the current value of the counter (q). When the counter reaches 9 (4'b1001), the T input is set to 1 to toggle the next flip-flop and reset the counter to 0.

# LOGIC DIAGRAM

![image](https://github.com/varsha-2005/Simulation-project--Digital-Electronics/assets/119288183/b55acd10-ade1-48a7-9f5e-80d0b58bf543)


# NETLIST DIAGRAM


![Screenshot (121)](https://github.com/varsha-2005/Simulation-project--Digital-Electronics/assets/119288183/4a673a0f-5c4c-4279-ac05-ba580a2053b7)

# TIMING DIAGRAM

# PROGRAM

# REFERENCE
