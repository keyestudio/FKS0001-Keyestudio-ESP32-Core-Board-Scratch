

# **Project 16: Timebomb**

### **1. Description**

This project will give you an opportunity experience an interesting timebomb game.  

In this project, the dot matrix represents your timebomb, while the digital tube displays remaining time. Buttons can not only control the bomb but also set its time. You may set a countdown to control this bomb, and it explodes when the countdown is over. Beyond that, a buzzer is adopted to alarm. 

Anyhow, by programming on multiple sensors, your comprehensive capability of logic thinking can be enhanced. 

### **2. Flow Chart**

![16-导出](./media/161616.png)

### **3. Wiring Diagram**

![](./media/16-1682065508572-74.jpg)

### **4. Test Code **

1. Drag the two basic blocks.

   ![image-20230324153753531](./media/image-20230324145038355.png)

2. Set the button pin to “input”.

![image-20230420142108112](./media/image-20230420142108112.png)

3. Add an "init matrix display" block from "Matrix" and set the pin CS to IO15. What follows it are a "brightness" block with its value of 3 and a "variable" block (set variable type to int and name to item, assign 0 as its initial value).

![image-20230420142137230](./media/image-20230420142137230.png)

4. In "Matrix", drag a "fill color" block and select "black"(i.e. all LED go off to clear previous display). Add a "display image" to define a smile face. Then, put a refresh block to renew the display. 

![image-20230420142214440](./media/image-20230420142214440.png)

5. Drag an"if" block and fill the condition box with "interface IO33 button was be pushed?". Add a "variable mode" block after "then" and set its name to item and mode to "++".

![image-20230420142340866](./media/image-20230420142340866.png)

6.  Repeat the operation in step 5, but set the interface to IO32 and the mode to "- -".

![image-20230420142417271](./media/image-20230420142417271.png)

7. Drag an "if" block to judge whether pin IO26 is pushed. In this "if", we add a repeat block and set its condition to "item" = 0 . 

In the "repeat until" loop, put a "variable mode" and set "item" to "- -", as shown below. Drag a "TM1650 display" block from "Digital tube" and define the showing string as "variable item" block. Then add a "buzzer output" block and set output to HIGH at pin IO27 followed by a 0.5s delay. Re-operate the last procedure but set the output to LOW. 

![image-20230420142530355](./media/image-20230420142530355.png)

8. Program another loop code and define the condition as "interface IO25 button was be pushed?". The following executions are in this loop. Put a "TM1650 display" block and define the showing string as "variable item" block.  Then repeat step 4 but here we set the image to a crying face. 

![image-20230420142630314](./media/image-20230420142630314.png)

9. Drag an "if then" block and fill the blank with a condition: item ＞ 9999. Add a statement "set item variable by 0" in this condition block. 

![image-20230325162514307](./media/image-20230325162514307.png)

10. Drag a "TM1650 display" from "Digital tube" and define the showing string as "variable item". For the same, don't forget to delay 0.2s.

![image-20230325162611261](./media/image-20230325162611261.png)

**Complete Code:**

![](./media/16-1681971468336-29.png)

### **5. Test Result**

After connecting the wiring and uploading code, press blue button to add time, green to reduce and red to reset. Press yellow button for counting down. When it is over, the bomb explodes. 

