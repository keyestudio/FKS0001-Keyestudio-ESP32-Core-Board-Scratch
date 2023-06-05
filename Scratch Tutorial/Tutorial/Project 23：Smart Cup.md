# **Project 23: Smart Cup**

### **1. Description**
In this project, we mainly adopt the Arduino development board to create a programmable smart cup, which reveals the temperature of inner liquid through a RGB indicator. It can control the brightness of the light by setting a temperature threshold. If the threshold is exceeded, it will get brighter. Otherwise, it gets darker. 

The smart cup enables to help users better control the temperature of their drinking water and effectively prevent overheating or freezing.

### **2. Working Principle**

![img-20230225082723](./media/img-20230225082723.png)

Related settings in DHT11 is provided by manufacturers, so you only need to orderly read and process data according to its sequence chart. 

Besides, the relevant codes are packaged in our libraries, which is convenient for you to set pins and read values. 

### **3. Wiring Diagram**

![23-1](./media/23-1.jpg)

### **4. Test Code**

1. Drag two basic blocks. Add the serial baud rate module and set the baud rate to 9600.

2. Drag the DHT module from “Temperature and humidity” and set the pin to IO26, mode to dht11.

![image-20230421092757020](./media/image-20230421092757020.png)

3. Add serial print module with no-wrap, and set the print to “RH:”, then follow the steps below, and add a delay of 1s.

**Complete Code:**

![](./media/23-2.png)

### **5. Test Result**

After connecting the wiring and uploading code, click ![image-20230320142348367](media/image-20230320142348367.png) to open serial monitor to set baud rate to 9600, and the temperature and humidity value will be displayed.

![](./media/image-20230420172812419.png)

### **6. Expansion Code**

In this expansion experiment, we will make a smart cup which can show liquid temperature. We divide 100 into four parts with an LED representing for each: 

**Red LED: ** 100-75°C
**Yellow LED: ** 75-50°C
**Green LED: ** 50-25°C
**Blue LED:**  25-0°C

**Flow Chart：**

![](./media/1679903142983-34.png)

**Wiring Diagram：**

![](./media/23-2.jpg)

**Code：**

1. Drag two basic blocks. Then set the 4 LED pins to “output” , the DHT11 pin to IO26, mode to dht11 and the variable name to temp.

![image-20230421091902544](./media/image-20230421091902544.png)

2. Assign the temperature value of DHT11 to the variable temp

![image-20230421092022788](./media/image-20230421092022788.png)

3. Use the "if else" to judge the variable temp. If the conditions are met, the corresponding LED will be on, otherwise it will be off. 

   

**Complete Code:**

![](./media/23-2-1682038142026-3.png)

### **7. Code Explanation**

1. In this code block, the marked number can be filled in the blank so that multiple temperature and humidity sensors can be connected. After setting the pin and mode, the value can be read. In this project, we set the mode to DHT11.
   ![](./media/image-20230421092208158.png)
2. Read the temperature and humidity code block.
   ![](./media/image-20230421092234397.png)

