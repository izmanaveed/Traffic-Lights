# Traffic Lights Project
Our project has two parts:  
1-Implementation of a single-way traffic control system on a breadboard  
2-Implementation of 4-way traffic control system on FPGA

# PART 1: Implementation of a single-way traffic control system on a breadboard
This project will use IC 555 as an Astable Multivibrator for rapid square wave pulse generation. Astable Multivibrator mode of 555 timer IC is also called Free running or self-triggering mode. It has two stable states (HIGH and LOW). This clock pulse will be fed to IC 4017 which is a Counter IC. In this counter IC, for every pulse fed to input pin-14, the High-level output keeps shifting from Q1 to Q9 in cyclic order.
One output is higher and the other output pins of the IC remain at a low state.

## COMPONENTS:
NE555 (Timer IC)  
CD4017B (Counter IC)  
IN4148 Diode(x6)  
1KΩ Resistor(x3)  
10KΩ Resistor  
22KΩ Resistor(x2)  
100KΩ Resistor  
47µF Electrolytic Capacitor  
0.01µF Ceramic Capacitor  
6.8nF Ceramic Capacitor  
Red, Yellow, Green LEDs  
9V Battery  
Wires  
Battery Clip

## CONSTRUCTION:
We have two ICs i.e. IC 4017 and NE 555 timer.  
Pin 1,5,6,9 are shorted and then connected to a 1k resistor which is then connected to anode of green LED.   
Pin 11 and 10 are shorted and then connected to a 1k resistor which is then connected to anode of yellow LED.   
Pin 12 is connected to a 1k resistor connected to the anode of the red LED.  
The cathodes of the LEDs are connected to the negative terminal of the battery.  
Pin 8 and 13 are shorted. One end is connected to the negative terminal of the battery, the other end is connected to a 100k resistor. The 100k resistor is connected to a 6.8Nf whose one end is connected to the positive terminal of the battery and its other end is connected to pin 15.  
Pin 16 is connected to the positive terminal of the battery.  
Pin 14 is connected to a 10k resistor connected to pin 3 of the 555 timer IC.  
Now we shall see the connections of 555 IC:  
Pins 4,8 are connected to the positive terminal of the battery. Pin 1 is connected to the negative terminal of the battery.  
A 0.01 microF is connected to pin 5. Its other end is connected to the negative terminal of the battery.  
Pins 2 and 6 are shorted. One end of this short circuit is connected to a 47 microF capacitor, whose other end is connected to the negative terminal of the battery, and its other end is connected to a 22k resistor. One end of the 22k resistor is connected to pin 7 of the IC which is further connected to another 22k resistor which is then connected with the positive end of the battery.

## CIRCUIT DIAGRAM:
![image](https://github.com/izmanaveed/Traffic-Lights-DLD/assets/59065717/a43b1490-bad9-46ec-8799-fa8f90f09a5b)

![proteus](https://github.com/izmanaveed/Traffic-Lights-DLD/assets/59065717/e01c100b-01aa-4aff-bcf6-99f31cb9e77a)

## WORKING:
This traffic light is made with the help of counter IC, which is mainly used for Sequential Circuits. We can also call it as Sequential Traffic Lights. Sequential Circuits are used to count the numbers in the series. Coming to the working principle of Traffic Lights, the main IC is 4017 counter IC which is used to glow the Red, yellow and green LED respectively. 555 timer acts as a pulse generator providing an input to the 4017 counter IC. Timing of glow of certain lights depends upon the 555 timer’s pulse. LEDs are not connected directly with 4017 counter, as the lights won’t be stable. Main drawback of this circuit is that you can never have an exact timing with this, however you will have best estimated.


# PART 2: IMPLEMENTATION OF -WAY TRAFFIC CONTROL SYSTEM ON FPGA
### State Table:
![image](https://github.com/izmanaveed/Traffic-Lights-DLD/assets/59065717/734b8d83-709b-4cfe-8f72-f14eff195dad)
### Time Delay: 
![image](https://github.com/izmanaveed/Traffic-Lights-DLD/assets/59065717/f9a4a062-a064-4799-b713-919a26943eaf)



