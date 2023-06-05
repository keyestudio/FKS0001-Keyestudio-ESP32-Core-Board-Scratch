



# **Project 2: Breathing LED**

### **1. Description**

Arduino breathing led utilizes on-board programmable PWM to output analog waveform. After powering on, LED brightness can be adjusted through duty cycle of the waveform to eventually realize the effect of breathing led. 
In this way, ambient light can be simulated by changing LED brightness over time. Also, breathing led can form a colorful mini light to construct a tranquil and warm environment.

### **2. What is PWM?**

PWM controls analog output via digital means, which is able to adjust duty cycle of the wave (a signal circularly shifting between high level and low level).

For Arduino, digital ports of voltage output are LOW and HIGH, which respectively correspond to 0V and 5V. Generally, we define LOW as 0 and HIGH as 1. Arduino will output 500 signals of 0 or 1 within 1s. If they are "1", 5V will be output. Oppositely, if they are all 0, the output will be 0V. Or if they are 010101010101..., the average output will be 2.5V. 

In other words, output ratio of 0 and 1 affects the voltage value, the more 0 and 1 signals are output per unit time, the more accurate the control will be. 


![](./media/img-20230225090854.png)

### **3. Wiring Diagram**

![1](./media/1-1682063240823-51.jpg)

### **4. Test Code**

We adopt "for" statement to increase a variable from 0 to 255, and define the variable as PWM output (analogWrite(pin, value)). By the way, a delay time may reinforce the control of LED shining time. Next, we use another "for" statement to decrease it from 255 to 0 with a delay time to control LED dimming process. 

1. Drag the two code blocks.

![image-20230324145038355](./media/image-20230324145038355.png)



2. Drag the following block from "Variables" part, and define the name to "item" with an initial assignment "0". Put this block in "forever" block. 

![image-20230324145311206](./media/image-20230324145311206.png)

3. Drag  the following block from "Control" part and set it to 255 times, which is the maximum value of PWM.

![image-20230324145621946](./media/image-20230324145621946.png)

4. Drag the following block from "Variables" part, put "item" as its changed object and set the mode to "++".

![image-20230324145715047](./media/image-20230324145715047.png)

5. Drag the following block from “LED” part and set the LED pin to IO5. Then add an "variable" block in it and fill in the blank with "item". 

![](./media/image-20230420101030817.png)

6. Drag the following block from "Control" part and set the time to 0.01s , that is 10ms. 

![image-20230324150616342](./media/image-20230324150616342.png)

7. According to previous steps, build another code block with the only difference of variable mode "– –".

![](./media/image-20230420101547508.png)

**Complete Code：**

![](./media/2-1681956580087-14.png)

### **5. Test Result**
After uploading the code, we can see the LED dims gradually. It "breathes" evenly.
### **6. Code Explanation**

1. This block is used to set variable usable range, variable type , name and its initial value.
   ![Img](./media/img-20230307190132.png)
2. Repeating times can be assigned in the blank of this repeat block. 
   ![Img](./media/img-20230307190325.png)
3. Input a variable name in the blank and its value will add 1 each time the code executes. "++" can be altered to "– –".
   ![Img](./media/img-20230307190714.png)
4. Input a variable name in the blank and its value will reduce 1 each time the code executes.  "– –" can be altered to "++" . 
   ![Img](./media/img-20230307192056.png)
5. This is a PWM output module, and the white box is the value of the output PWM.
   ![](./media/image-20230419112540092.png)

