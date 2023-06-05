

# **Project 10：Dot Matrix Display**

### **1. Description**
This module consists of a 8x8 LED dot matrix with one control pin for each row as well as each column to adjust the brightness of LED. Connecting with Arduino board, the brightness of LED is controlled to display characters and figures via Arduino programming. In this way, simple characters, numbers and figures are able to be displayed. It also can be applied in game machines or screens.

![img-20230225082512](./media/img-20230225082512.png)

MAX7219 is an IC with SPI communication and can be used to control the 8x8 dot matrix. The MAX7219 SPI communication has integrated in our libraries and you can recall directly.



### **3. Wiring Diagram**

![10](./media/10-1682064271698-61.jpg)

### **4. Test Code**

1.Drag the two basic code blocks.

![image-20230324153753531](./media/image-20230324145038355.png)

2.Drag a "init matrix display" from “Matrix” and set CS to IO15. DIN and CLK are fixed pin respectively to IO23 and IO18.

![](./media/image-20230420092204108.png)

3. Drag a "set brightness" block and set it to 3. 

![image-20230325090343317](./media/image-20230325090343317.png)

4. Drag a "image" block and choose heart icon.

![image-20230325090650972](./media/image-20230325090650972.png)

5. Add a "refresh" block at the end. 

![image-20230325090527357](./media/image-20230325090527357.png)

**Complete Code：**

![](./media/10-1681953696698-12.png)

### **5. Test Result**

After connecting the wiring and uploading code, a heart will be displayed on the dot matrix, as shown below

![](./media/20230420085055.png)

### **6. Code Explanation**

1. Set the CS pin. In the code, DIN is fixed to io23 and SLK to io18, while CS pin is optional. For convient wiring, we select io15.

   ![](./media/image-20230420085552242.png)

2. Draw pixels. This code block will light up or turn off pixels on the dot matrix by axis x and y, with red for on and black for off.

![image-20230318120021624](./media/image-20230318120021624.png)

3. Draw line. Locate the line by two group of coordinate points, also with red for on and black for off. 

![image-20230318120145212](./media/image-20230318120145212.png)

4. Show characters. We have add character libraries so you only need to type a letter to display it on the dot matrix. Besides, it must be used cooperatively with a "rotation 180°" block. 

  ![image-20230318130321293](./media/image-20230318130321293.png)

5. Show numbers. Similarly, you only need to type a number to display it on the dot matrix, and it also must be used cooperatively with a "rotation 180°" block. 

![image-20230318130346709](./media/image-20230318130346709.png)

6. Show scrolling character strings. Collocating a "rotation 180°" block, the specified scrolling strings will be displayed after setting its speed. 

![image-20230318130405179](./media/image-20230318130405179.png)

7. Display image. For convenience, we have already integrated some emotion icons which can be selected directly. 

![image-20230318130421059](./media/image-20230318130421059.png)

8. Display fill colors. You may set to black (LED goes off) or red(LED lights up).

![image-20230318130444192](./media/image-20230318130444192.png)

9. Refresh the display. The dot matrix must be refreshed if it displays something. Or else, an error may occur.

![image-20230318130500471](./media/image-20230318130500471.png)

10. Set the brightness. You can lower the brightness when debugging to avoid offending to your eyes.

![image-20230318133821875](./media/image-20230318133821875.png)

11. Set rotation angles. For high compatibility with more code, some data and icons need a rotation with the avoidence of inverted display.  That is why a "rotation 180°" block is necessary in codes. 

![image-20230318133843286](./media/image-20230318133843286.png)

