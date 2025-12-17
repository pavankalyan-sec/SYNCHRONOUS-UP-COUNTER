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
~~~
1.Initialize the shift register to a known state (e.g., all zeros).

2.Input a bit serially into the shift register.

3.Shift the contents of the register one position to the right (or left).

4.Output the shifted bit from the last stage of the register.

5.Repeat steps 2-4 for each bit you want to input and shift.
~~~

**UP_COUNTER**
**PROGRAM**
<img width="417" height="275" alt="Screenshot 2025-12-17 201259" src="https://github.com/user-attachments/assets/31ca0482-d208-484f-b9f2-2eee8bb68e27" />

~~~
Developed by: Pavan Kalyan P
RegisterNumber: 25010044
~~~

**RTL LOGIC UP COUNTER**
<img width="753" height="256" alt="Screenshot 2025-12-17 201317" src="https://github.com/user-attachments/assets/aea0f575-9ce2-486c-914c-d7fd8bec70d3" />

**TIMING DIAGRAM FOR IP COUNTER**
<img width="1918" height="357" alt="Screenshot 2025-12-17 201703" src="https://github.com/user-attachments/assets/3a286f15-9161-4b44-83dd-4e4a0624f897" />

**TRUTH TABLE**
<img width="618" height="811" alt="image" src="https://github.com/user-attachments/assets/5b9c2700-bd83-432b-8b80-172c3ac3f5a3" />


**RESULTS**
Hence a 4 bit synchronous up counter is implemented correctly

**DOWN_COUNTER**
**PROGRAM**
<img width="508" height="264" alt="Screenshot 2025-12-17 201945" src="https://github.com/user-attachments/assets/361ba09f-720a-40c3-aa43-8be87018a7ca" />
<img width="487" height="254" alt="Screenshot 2025-12-17 203158" src="https://github.com/user-attachments/assets/6a2db5f3-f0c2-4e8d-9dc8-56cdbe6ee844" />

~~~
Developed by: Pavan Kalyan P
RegisterNumber: 25010044
~~~

**RTL LOGIC UP COUNTER**
<img width="631" height="257" alt="Screenshot 2025-12-17 202038" src="https://github.com/user-attachments/assets/aee7996d-5f36-4eaa-9635-0a32bcf6454f" />

**TIMING DIAGRAM FOR IP COUNTER**
<img width="1919" height="604" alt="Screenshot 2025-12-17 202259" src="https://github.com/user-attachments/assets/622125d9-e893-4a81-9193-ea364de12a94" />

**TRUTH TABLE**
<img width="707" height="710" alt="image" src="https://github.com/user-attachments/assets/20c4117e-0754-4067-9b14-aacdd67b39a7" />

**RESULTS**
Hence a 4 bit synchronous down counter is implemented correctly
