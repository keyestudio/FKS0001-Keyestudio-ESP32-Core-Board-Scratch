

# **Project 14: Counter**

### **1. Description**
Arduino 4-bit digital tube counter can record numbers within 0~9999. It features display speed, count mode adjustment as well as reset function. This module is wildly applied in real-time counter (such as button-press and DC motor rotation count), gaming and experiment equipment.

### **2. Flow Chart**

![](./media/1679466016942-28.png)

### **3. Wiring Diagram**

![14](./media/14-1682064654059-68.jpg)

### **4. Test Code**

1. Drag the two basic blocks.

![image-20230324153753531](./media/image-20230324145038355.png)

2. Set the button pin to “input”.

![image-20230420112313446](./media/image-20230420112313446.png)

3. put a "variable" block. Set the variable type to int and name to item. Assign 0 as its initial value. 

![image-20230420112430293](./media/image-20230420112430293.png)

4. Drag an "if" block from “Control” (it executes only when its condition is satisfied). Put a “Button pressed” block from “Button” to the condition box(the hexagon one) and set the pin to IO19. Drag a "variable mode" block and put it after "then", and define it as "item" and set the mode to "++".

   ![image-20230420112508168](./media/image-20230420112508168.png)

5. Repeat step 4, but set the interface to IO18 and mode to "– –".

![image-20230420112522534](./media/image-20230420112522534.png)

6. Drag another "if" block from “Control” and define its condition that "interface IO17 button was be pushed?". Put a variable setting block after "then" and set the "variable by 0".

![image-20230420112540247](./media/image-20230420112540247.png)

7. Drag a "if" block from “Control”. Find the "＞" block in “Operators” and fill the left blank with "variable item" and the right with "9999". Also, put a variable setting block after "then" and set the "variable by 0".

![image-20230325143340106](./media/image-20230325143340106.png)

8. Drag a "TM1650 display" block from "Digital tube" and set the displayed string to "variable item" block. Finally, don't forget to add a 0.2s delay. 

![image-20230325143541796](./media/image-20230325143541796.png)

**Complete Code:**

![](./media/14-1681961245533-25.png)

### **5. Test Result**

After connecting the wiring and uploading code, press green button to add 1, yellow to minus 1, and red to reset. 

### **6. Code Explanation**

**">"** block is used for judgment between two values. These two blanks can be replaced with either numbers or variables. 

![image-20230325144251951](./media/image-20230325144251951.png)

