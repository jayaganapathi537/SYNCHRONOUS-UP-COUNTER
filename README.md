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


1.Initialize the shift register to a known state (e.g., all zeros).


2.Input a bit serially into the shift register.


3.Shift the contents of the register one position to the right (or left).


4.Output the shifted bit from the last stage of the register.


5.Repeat steps 2-4 for each bit you want to input and shift.


**PROGRAM**


Program for flipflops and verify its truth table in quartus using Verilog programming. 


**Developed by: JAYAGANAPATHI S** 


**RegisterNumber:24900059**


![Screenshot 2024-12-11 135450](https://github.com/user-attachments/assets/f6b5d0eb-dbe5-4da4-b3f5-285472d71c90)


**RTL LOGIC UP COUNTER**


![328450512-ba5f33f2-0a46-4071-9de6-4f05e2d4caa6](https://github.com/user-attachments/assets/4cff2373-2f41-4809-970e-8343c00c1df5)


**TIMING DIAGRAM FOR IP COUNTER**


![328450615-b932b6cd-aa6e-4078-a348-235a71978f13](https://github.com/user-attachments/assets/d7ccb30f-35dd-473d-8729-6fdb1e4be938)


**TRUTH TABLE**


![328450787-c2bda272-5c6f-4c93-91f0-7f4783432c7d](https://github.com/user-attachments/assets/52fee0c9-c6a0-4c82-b69e-dec8a98685b4)


**RESULTS**


Hence a 4 bit synchronous up counter is implemented correctly.
