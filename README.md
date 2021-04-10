# Blinking_STM32
Simple Blinking Application using STM32

**Short Introduction on Ramping up the Blinky application**

**Configuration:**
1. Blink will be use LED2 integrated on the board by controlling PA5.
2. Using STMCUBEMX to configure board, pinout and IDE.
3. IDE will be using is keil.


**Instruction:**

Step 1: Set up code in STM32 Cube IDE 

For starting, STM32F446RE had been selected as the microcontroller in the MCU/MPU Selector tab for the simulation. Then, in the Pinout and Configuration tab, pin PA5 (Port A, Pin 5) had been used as GPIO. This pin is connected to LED on the board and acts as output for blinking. After all pinout is configured, browse directory which be using to store all project folder on Project Manager tab. After that, select type of IDE which in this demonstration we are using MDK ARM Keil to write code. Finally, click Generate button to force the tools to automate the template of the code in Keil. 
  

STEP 2: Make the LED blinking  
**Note: can straight away download all the file above and continue in KEIL IDE for the coding (Open KEIL project in: MDK-ARM > Blinking_app.uvprojx)**

For writing the Blinky code, there are various way to make LED turn ON and OFF. There are two examples for this. 

First example, we utilized toggle method:

**HAL_GPIO_TogglePin(GPIOA, GPIO_PIN_5);** 

**HAL_Delay(500);** 


For second example, we utilized write pin method which write “1” or “0”:

**HAL_GPIO_WritePin(GPIOA, GPIO_PIN_5, GPIO_PIN_SET);** 

**HAL_Delay(500);** 

**HAL_GPIO_WritePin(GPIOA, GPIO_PIN_5, GPIO_PIN_RESET);** 

**HAL_Delay(500);** 

  

The LED will be seems to turn ON and OFF with 0.5 seconds respectively based on values put in the HAL_DELAY. 


More details: 

Short simulation video : 
https://youtu.be/2vouni4_9io 
