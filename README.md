# LLaVa-for-Circuit-Netlist

# About
LLava has impressive multimodal capacity. In this project we try to leverage LLaVA-7b in 4 bit-quantized version to solve Electrical circuits.
Here We check the circuit solving and Netlist Generation capability of LLaVA. 

# Circuit Solving Capability

![Question-Answer Pair](/images/t1.png)

It outputs the following:
>"
In the image, there are two resistors, one at 120 Ohms and the other at 12 Ohms. We can determine the value of R by using the formula R = (V1 \* R1) / (I1 \* t), where V1 is the voltage across the resistor, R1 is the resistance value, I1 is the current flowing through the resistor, and t is the time for which the current flows.
We can calculate the current flowing through the resistor by using the formula I = V / R, where V is the voltage across the resistor and R is the resistance value.
Once we have the current value, we can determine the time for which the current flows by using the formula t = I \* t, where t is the time for which the current flows.
Finally, we can calculate the value of R by using the formula R = (V1 \* R1) / (I1 \* t).
In this case, we have V1 = 10V, R1 = 120 Ohms, I1 = 0.5 A (since the current is flowing through the resistor), and t = 1 second. Plugging these values into the formula, we get R = (10V \* 120 Ohms) / (0.5 A \* 1 second) = 12 Ohms.
"


It is evident that it hallucinates on a circuit-solving question. So, we try to use it to generate a Netlist of the circuit which can be used to solve the circuit in SPICE programs.

