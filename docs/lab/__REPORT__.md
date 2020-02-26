---
title: lab 3 report
author: Josh Bartolome  
partner: Kylie Urasaki
date: 2/25/20
---
# Task number X-X

During the lab, follow the steps in the Workbook, and complete the following.
- Fill in the code snippets to complete your design.
- Demonstrate behavioral simulation to the TA.
- Demonstrate timing simulation to the TA (if required).
- Demonstrate the implementation (with the Basys 3 board) to the TA.

In the report, complete the following.
- Explain the objective of the task.
- Include all your project codes in the [codes/lab](../../codes/lab) folder,
  if required.
- Explain your code.
- Include screenshots of the simulations in this folder, and insert them into
  the markdown file.
- Explain why the simulations are correct.
- Include pictures of the Basys 3 board running your implementation, and
  insert them into the markdown file.
- Explain why the implementation is correct.
- Conclude with the problem you encounterd during the task.

# Task number 1-1

The objective of this task was to create a 3 - 8 line decoder using the given truth table. 

The code is similar to our 7-segment code from the previous lab. Where the 3-bit input is translated from binary to decimal than evaluated in the case statement to make the correct output. For each decimal value of 0 to 7, set the 8-bit output. The 0 or 1 following the “8’b” determine which bit of the output is to be on. With 1 meaning that output is to be on while the 0 means the LED should remain off.  

![](lab3_1_1_schematic.png)










![](lab3_1_1_sim.png)


The simulation above shows all the possible inputs and outputs of the code. With each input, the value was translated from binary to decimal. When comparing the values to the truth table, when the input is 0, the output is 1. When the input is 1, output is 2. When input is 2, output is 4, and so on.

In conclusion this task was fairly easy, as it was pretty similar to Lab 2. With our gained knowledge of case statements, we were able to decode 3-bit inputs into 8-bit outputs.

# Task number 1-2

The objective of this task is to design and implement a popular IC, 74138, functionality with the decoder used in part 1-1. The IC symbol and the truth table for this task were also given and used.

The code for this task was very similar to the code written and used in task 1-1. Where the code used is similar to a 3-to-8 decoder. The main difference is that the code used in this task has more control, or enable signals. Which in certain systems would help to simplify decoding. The code first will see if the input g2a_2 is 1 and if it is it will set the output y to 8'b11111111, and if the input g2b_n it will also set y to 8'b11111111 and then finally will check if g1 is 0, and if it is, it will also set y to 8'b11111111. And after all of that it will go through the case statement with many different outcomes.
![](lab3_1_2_schematic.PNG)


![](lab3_1_2_simulation.PNG)



The simulation shows the possible inputs and outputs within 200 ns which is the timing that the simulation was run in. The simulation shows the inputs and outputs stated and given in the code and shown in the truth table.

# Task number 2-1

The objective of this task is to design an 8 - 3 priority encoder with the given truth table. Secondly, to learn about how encoder circuits transfer information from one format to another. For this task, we used behavioral modeling in a similar format as task 1-1.

In the code, we used behavioral modeling to create two case statements. The coding is similar to the previous task, but going from an 8 - 3 bit. The “x” represent numbers that we don’t want the computer to consider. These are called “don’t care” values. For the first case statement, it converted the eight-bit data inputs to three-bit data outputs using the truth table given in the tutorial and set that to the output y. We initialize y as 1 to make all the leds off for implementation. The second case statement is to assign the eight-bit data inputs to the gs output and make it equal to values in the truth table. We initialize gs as 1 to make all the leds off for implementation.



![](lab3_2_1_schematic.png)


The schematic shows the 8 bit input being evaluated in the boards to determine the output. Based on the bits that are switched on, each board will determine the outputs based on the case statements. The board evaluating for the y output is much larger than the one for the gs output because there are more outputs to be produced for y than gs. Additionally, the output is disconnected as it was determined that the enabler was not needed as people were having a hard time with it. However, the basic objective, in that the schematic allows the 3 lights to light up in binary given an input.

In conclusion, we initially had trouble with coding. We also had small issues that affected our code like in the first case statement the “x” didn’t work, but when we switched it to “0” the code was able to work. Also understanding how to use don’t cares and how that translates to the design was difficult.

