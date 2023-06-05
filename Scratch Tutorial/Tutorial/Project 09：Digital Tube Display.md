# **Project 9：Digital Tube Display**

### **1.  Description**
This 4-Digit tube display is a device used to display counting or time, which is able to  display numbers from 0 ~ 9 and simple letters. It consists of four digital tubes, each of which has seven light-emitting diodes (LED). 

Moreover, multiple functions can be realized by connecting their pins to the Arduino development board, such as timekeeping and some game storing. 

### **2. Working Principle**

![img-20230225082040](./media/img-20230225082040.png)

TM1650 utilizes IIC protocol and adopts two bus lines (SDA and SCL).

The code is provided in our blocks, and the digital tube will display numbers via this code. 

### **3. Wiring Diagram**

![9](./media/9.jpg)

### **4. Test Code**

To show numbers on the display, you only need to drag a "TM 1650 display" block from "Digital tube" and set the number string to 9999.

![9-1](./media/9-1-1681951089602-7.png)

### **5. Test Result**

After connecting the wiring and uploading code, the digital tube display shows "9999", as shown below.

![image-20230321161936665](./media/image-20230321161936665.png)

### **6. Extended Code**

Let's have some difficult operations. Rather than static numbers, we handle it to show some dynamic ones. 
The following code manipulates the tubes to display 1~9999.

1. Drag the two basic code blocks.

   ![image-20230324153753531](./media/image-20230324145038355.png)

2. Drag the following block from "Variables". Set the type to int and name to item, and assign 0 as its initial value.

![image-20230325084909953](./media/image-20230325084909953.png)

3. Drag the following block from "Control" and set to 9999 times.  

![image-20230325085129944](./media/image-20230325085129944.png)

4. Drag a "variable mode" from "Variables", define its name to item and set the mode to "++".

5. Drag a "TM 1650 display" block from "Digital tube" and replace the string value with variable item. Add a delay time of 0.5s after it. 

![](./media/image-20230420084113414.png)

6. Add a "set variable" block after the "repeat" block. Set item variable by 0. Otherwise, the item value will be out of display range after 9999 loops.

![image-20230325085754198](./media/image-20230325085754198.png)

**Complete Code：** 

![9-2](./media/9-2.png)

### **7.  Code Explanation**

1. Set the display string. Directly type numbers or letters you want to display in the blank

![image-20230420084225223](./media/image-20230420084225223.png)

2. Set the ON or OFF of this TM 1650 digital tube. Each tube can be controlled separately. 

![image-20230420084238883](./media/image-20230420084238883.png)

3. It is able to clear the display or used as a master switch to turn on or turn off the digital tube. 

![image-20230420084253032](./media/image-20230420084253032.png)
