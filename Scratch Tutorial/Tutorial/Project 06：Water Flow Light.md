

# **Project 6：Water Flow Light**
### **1. Description**

This simple water flow light project enables to help you learn electronic packaging. In this project, we will control LEDs to change the color in a specified speed via a Arduino board.

### **2. Wiring Diagram**

![6](./media/6.jpg)

### **3. Test Code**

A water flow light consists of a stream of LED lighting from left to right.

1. Drag the two basic code blocks.

   ![image-20230324153753531](./media/image-20230324145038355.png)

2. Set the pin mode to “output”

![image-20230419171700652](./media/image-20230419171700652.png)

2. Drag the following blocks from "LED" part and set the IO15 pin to LOW, the IO12 pin to HIGH. Then set the delay time to 0.2s.  

![image-20230419171826488](./media/image-20230419171826488.png)

3. Drag the following blocks from "LED" part and set the IO12 pin to LOW, the IO13 pin to HIGH. Then set the delay time to 0.2s.  

![image-20230419172058520](./media/image-20230419172058520.png)

4. Drag the following blocks from "LED" part and set the IO13 pin to LOW, the IO14 pin to HIGH. Then set the delay time to 0.2s. 

![image-20230419172145604](./media/image-20230419172145604.png)

5. Drag the following blocks from "LED" part and set the IO14 pin to LOW, the IO15 pin to HIGH. Then set the delay time to 0.2s.  

![](./media/image-20230419172156313.png)

**Complete Code：**

![](./media/6-1681896195909-19.png)

### **4. Test Result**

After uploading code and powering on, the LEDs light up from left to right.





