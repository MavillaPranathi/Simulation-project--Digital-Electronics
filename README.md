# TITTLE

Design and simulate 2 bit synchronous upcounter with T flip flop using Verilog.

# THEORY

1. The module sp declaration defines the module name (sp) along with its input and output ports. In this case, it has an input port clk representing the clock signal and an output port a representing the 2-bit parallel output
 
2. The always @(posedge clk) block indicates that the following statements will execute only on the positive edge of the clock signal (clk). This ensures that the circuit operates in a synchronous manner.

3. Inside the always block, two assignments are performed.

       a[1] = (a[0]) ^ a[1]; updates the value of the second bit (a[1]) in the output register a. It uses the XOR (^) operation between the current value of the            first bit (a[0]) and the current value of the second bit (a[1]). This XOR operation introduces feedback into the circuit.

       a[0] = 1 ^ a[0]; updates the value of the first bit (a[0]) in the output register a. It performs an XOR operation between the constant value 1 and the            current value of the first bit (a[0]). This effectively alternates the value of the first bit between 0 and 1 on each clock cycle.
       
4. The combination of these two assignments creates a shift register with feedback behavior. The feedback connection is established by XORing the first bit (a[0]) with the second bit (a[1]). This feedback ensures that the second bit reflects the value of the previous first bit on each clock cycle. The first bit alternates between 0 and 1.

5. By observing the output a over multiple clock cycles, you will see the input bit being serially shifted into the shift register and the feedback XOR operation modifying the values in the shift register.
# LOGIC DIAGRAM

# NETLIST DIAGRAM


# TIMING DIAGRAM

# PROGRAM

# REFERENCE
