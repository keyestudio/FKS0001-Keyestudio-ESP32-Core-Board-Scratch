# **Project 1: LED Blinking**

###  **1. Description**

LED blinking is a simple project designed for starters. You only need to install an LED on Arduino board and upload the code on Arduino IDE. This project reinforces the learning of Arduino conceptual framework and using methods for starters. 

###  **2. Working Principle**

![](./media/led-1684551913165-2.png)

**LED:** Generally speaking, limited IO ports of output current may cause low brightness of LED, so a NPN triode (Q2) is applied in circuit as a switch. In this case, the LED will light up if the base(pin 1) of triode is at a high level. On the contrary, LED goes off when the base is at low. 

**Triode switch:** Briefly, LED lights up when the base(pin 1) is at a high level. In the same breath, the collector(pin 3) and emitter(pin 2) are connected, and then VCC passes through a current-limiting resistor to LED and finally to GND, which forms a circuit. On the contrary, LED goes off when the base is at low. In this circumstance, the collector and emitter are disconnected  and the LED lights off.



### **3. Wiring Diagram**

![1](./media/1.jpg)

###  **4. Test Code**

According to previous principles, we can control LED via levels of pins on the development board.

1. Drag  the following block in "Events" part. 

![image-20230324144129788](./media/image-20230324144129788.png)

2. Drag the following block  in "Control" part . 



![image-20230324144235832](./media/image-20230324144235832.png)

3. Drag the following block  in "Pins" part and set the IO5 pin to output.

![](./media/image-20230419144736421.png)

4. Drag the following block  in "LED" part and set the IO5 pin to HIGH.

![](./media/image-20230420101235993.png)

5. Drag the following block  in "Control" part . 

![image-20230324144523478](./media/image-20230324144523478.png)

6. Drag the following blocks and set the IO5 pin to LOW. 

![](./media/image-20230420101253873.png)





**Complete Code：**

![](./media/1-1681887273768-8.png)



###  **5. Test Result**

After uploading the code and powering on, LED will be on for 1s and off for 1s.



### **6. Code Explanation**

**Note: Pin mode must be set to "output" ** **when using LED module**

1.Code blocks will not execute if the following block is not exist.

![Img-20230307162920](./media/img-20230307162920.png)
	2. Code blocks in  the following block will execute in a loop. 
![Img](./media/img-20230307164251.png)

2.It is a module used to set the pin mode(control LED and buzzer for “output” mode, and read sensor module for “input” ).

![](./media/image-20230419144739717.png)

3.It is a module used to set the pin and the levels("HIGH" and "LOW").
![](./media/image-20230420101235993.png)

4.It is a module used to set the delay time.
![Img](./media/img-20230307164630.png)

