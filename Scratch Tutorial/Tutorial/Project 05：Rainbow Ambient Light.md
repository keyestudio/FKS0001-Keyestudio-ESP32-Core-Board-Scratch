# **Project 5：Rainbow Ambient Light**

### **1. Description**

2812RGB LED is a programable colorful dreamy light, whose color, brightness and rhythm are adjustable.  This rainbow ambient light can be used as a dynamic decoration at will. Or you may control it to "dance with music". Importantly, it can be improved as an alarm. Its built-in sensor detects the ambient surroundings to warn users by changing  its color, brightness and rhythm.

### **2. Working Principle**

![image-20230314194251127](./media/image-20230314194251127.png)

The data protocol adopts communication mode of single-line return-to-zero code. After the pixel is reset on power, DIN terminal receives data from the controller. The firstly arriving 24bit data will be extracted by the first pixel and be sent to the inner data register. 

Remaining data will be amplified by an amplification circuit and be transmitted through DOUT port to the next cascaded pixel. 
Being transmitted through pixels, the signal decreases 24bit each time. 

Besides, The pixel adopts automatic shaping and forwarding technology, insomuch that the cascade number of the pixel is only limited by the signal transmission speed.



### **3. Wiring Diagram**

![5](./media/5.jpg)

### **4. Test Code**

Let's learn how to light up 2812 RGB and set its colors. 

1. Drag the two code blocks.

   ![image-20230324153753531](./media/image-20230324145038355.png)

2. Drag the following block from "RGB LED" part and set the pin to IO15 and the number of LED to 6.

![](./media/image-20230419153204292.png)

3. Drag the following block from "RGB LED" part and set brightness to 20. 

![](./media/image-20230419153243384.png)

4. Drag the following blocks and set the number of LED to 0 ,1, 2, 3, 4 and 5, then choose red, green, blue, yellow, purple and  white colors. 

![image-20230419153559804](./media/image-20230419153559804.png)

5. Add the following block.

![image-20230419153739964](./media/image-20230419153739964.png)



**Complete Code：**

![](./media/5-1-1681889952779-15.png)

### **5. Test Result**

After uploading code, connecting the wiring and powering on, the LED will light up in different colors, as show below:

![image-20230331150517106](./media/image-20230331150517106.png)

### **6. Knowledge Expansion**

In this expansion project, let's make a mini light show!

Nest four "repeat" blocks and add a "variable +" in them, then clear the corresponding variables to 0 at the end of each loop. 

![](./media/image-20230419164632176.png)

Put the above three variables in "RGB" block so that these color values are controlled. Then add a refresh module.

![image-20230324161152823](./media/image-20230324161152823.png)

Put the RGB in a "show color" block to display colors. And define a variable item to control the displayed LED.

![](./media/image-20230419165108703.png)

The forever module is used to control RGB LEDs, which will cycle from 0-5 to gradually light up each light.

![image-20230419164930530](./media/image-20230419164930530.png)

**Complete Code**

![](./media/5-2-1681893901460-17.png)

### **7. Code Explanation**

1. Set the number of 2812 RGB. A development board pin can control multiple 2812 RGB LEDs, so we need to set the number in advance and select the connected pin. 

![](./media/image-20230419165202324.png)

2. Set the brightness of 2812 RGB. Input the brightness value within 0-255, in which 255 is the brightest.

![](./media/image-20230419165248645.png)

3. This block will turn off all 2812 RGBs. 

![](./media/image-20230419165314775.png)

4. Control the display of 2812 RGBs. We can fill the blanks to control the lighting LED and its color after selecting the pin. For instance, "0 to 0" means only the first LED lights up. After uploading the code, the first LED will turn on in the set color.

   **NOTE:** The two blanks also can be filled with variables, so that a light show is able to be formed. 

![](./media/image-20230419165348171.png)

5. Set the color of 2812 RGBs. The displayed color can be modulated by the value in red, green and blue. We can add this block in the color settings of 2812 RGB.

   ![](./media/image-20230419165441257.png)

6. It can control a single 2812 RGB display via enter the control led number and select the color.

![image-20230419165850546](./media/image-20230419165850546.png)

7. The 2812 RGB will display the set color only after refreshing

![image-20230419170020802](./media/image-20230419170020802.png)
