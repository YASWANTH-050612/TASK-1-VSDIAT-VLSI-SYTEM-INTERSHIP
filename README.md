# TASK-1-VSDIAT-VLSI-SYTEM-INTERSHIP

## 1

# Verilog Code and FPGA Integration 

## 1. Verilog Code Overview

The Verilog code helps control the RGB LED. It has a few inputs and outputs that manage the red, green, and blue LED colors.

### Module Declaration 

- This declares about the input and outputs . 

### Key Inputs and Outputs:

- **Input:**
  - **hw_clk**: The clock signal for the FPGA.
        {clk -- clock}

- **Outputs:**
  - **led_red**, **led_green**, **led_blue**: These control the LED's colors.
  - **testwire**: This is just for testing.

### How It Works Inside:

- There’s an **Internal Oscillator** that makes the clock for the FPGA.
- A **Frequency Counter** counts the clock to control the LED colors.
- The **RGB LED Driver** takes care of showing the colors on the LED.

 {As told in the datashhet}
 
---

## 2. Pin Mapping (from the PCF file)

The **PCF file** shows where to connect things between the Verilog code and the FPGA board.

- **led_red** goes to **Pin 39**
- **led_blue** goes to **Pin 41**
- **led_green** goes to **Pin 40**
- **hw_clk** goes to **Pin 20**
- **testwire** goes to **Pin 17**

These connections were double-checked using the board’s datasheet to make sure everything was correct.

Note : That the PCF file shows that the pin 40 for the led_blue   ,  but on the board the led_blue  which was denoted by the {capital}"B" is showing 41

---

## 3. How to Use the FPGA

### Step 1 : Check the board manually
Checked the parts , and pin numbering which was given in the datasheet 

### Step 2: Connect the FPGA Board
Plug the FPGA into your computer using a **USB-C cable** with the extension pack and install **FTDI drivers**

### Step 3: Build and Flash the FPGA

To make everything work, I run these commands on my computer:

make clean       # This clears old files.
make build       # This compiles the code.
sudo make flash  # This loads the new code into the FPGA.

## Step 4: Check the RGB LED
Once done, I checked the LED to make sure if it lights up the right way, proving everything worked.

## 4. Problems and Fixes

### Pin Confusion:
There was a little mix-up with the blue LED pin, but after checking, we figured out it’s Pin 41 for **led_blue**.

### Connecting the Board:
Getting the FPGA connected to the computer using **USB-C** and **FTDI** took some time, but the board manual helped a lot.

## 5. Final Thoughts
This project helped me learn how to control the RGB LED with **Verilog**, how to set up pin mappings, and how to flash the **VSDSquadron FPGA Mini Board**. 

### 6. Some other obsevations and problems and slutions

First the VM is not recognising and it is a big deal

After sombodys and Sir's help I did everything we need to do for the recognisation it didnot work.

After one friend told me to reinstall and restart you will get  , yes I got it but it didn't started   

After 3 attemps it successfully came  ....

Unknowngly and unfortunately , I used multiusb cable which has 3 different cabbles , the second cable came contact to the first led which is used to  if  the PC is 
connected or not , so the LED is offed because of short circit So I thought it gone but with god,s grace the LED is only gone not the board .......

So , I used the single USB cable..


It was glad to learning these things !!!!!!!




