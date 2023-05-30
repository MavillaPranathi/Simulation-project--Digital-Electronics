# TITTLE

Design and simulate 2 bit synchronous upcounter with T flip flop using Verilog.

# THEORY

A 2-bit synchronous up-counter is a sequential circuit that counts sequentially from 00 to 11 and then wraps around back to 00. It has two output bits, representing the counter value. The counting operation is synchronized with a clock signal, meaning the counter increments its value only on a specific clock edge (e.g., rising edge or falling edge).

To implement a 2-bit synchronous up-counter using T flip-flops, you can follow these steps:

Step 1: Declare the input and output ports:
clk: The clock signal used to synchronize the counting operation.
reset: A reset signal that initializes the counter to 00.
count[1:0]: The 2-bit output representing the counter value.

Step 2: Internal signals and flip-flops:
Declare a 2-bit register to store the counter value, typically denoted as q.
Declare a single-bit input for the T flip-flop, usually denoted as t.

Step 3: Instantiate T flip-flops and connect them:
Instantiate two T flip-flops, one for each bit of the counter (q[1] and q[0]).
Connect the clock signal (clk) and reset signal (reset) to each T flip-flop.
Connect the output of the first flip-flop (q[0]) to the input of the second flip-flop (q[1]).

Step 4: Define the T input based on the counter value:
Use a combinational logic circuit (e.g., an if-else statement) to determine the T input for the T flip-flops.
When the counter is at the value 01, set the T input to 1. This will toggle the next flip-flop and increment the counter.
For all other counter values, set the T input to 0, so the counter remains unchanged.

Step 5: Assign the counter value to the output:
Assign the value of the 2-bit counter register (q) to the output ports (count[1:0]).
By following these steps, you can implement a 2-bit synchronous up-counter using T flip-flops. The counter will increment its value on each clock edge, following the defined logic for the T input. The reset signal can be used to initialize the counter to 00, ensuring predictable behavior when the circuit starts.

# LOGIC DIAGRAM

https://www.google.com/url?sa=i&url=https%3A%2F%2Fprogrammerbay.com%2Fdesign-a-2-bit-synchronous-up-counter-using-t-flip-flop%2F&psig=AOvVaw2CE9XkVV_vNpO9p6QPeEer&ust=1685533177190000&source=images&cd=vfe&ved=0CA4QjRxqFwoTCIDA3sj6nP8CFQAAAAAdAAAAABAE

# NETLIST DIAGRAM

![Screenshot (136)](https://github.com/MavillaPranathi/Simulation-project--Digital-Electronics/assets/118343610/d66d33e7-ac4f-443e-9c95-4609b090fc2d)

# TIMING DIAGRAM

![Screenshot (135)](https://github.com/MavillaPranathi/Simulation-project--Digital-Electronics/assets/118343610/6f45edce-5660-49ee-8657-f294c4327546)

# PROGRAM
DEVELOPED BY: M.PRANATHI
REFRENCE NUMBER: 212222240064

module sp (clk,a);
input clk;
output  reg [1:0]a;
always@(posedge clk)
begin
   a[1]=(a[0])^a[1];
	a[0]=1^a[0];
end
endmodule
# RESULT 
This project is successfully completed.
