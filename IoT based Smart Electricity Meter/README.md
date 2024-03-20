# IoT based Electricity Meter using ESP32 & Blink

In this project, we will learn how to make our own ***IoT Based Electricity Energy Meter using ESP32*** & monitor data on the **Blynk Application**. Earlier we built IoT DC Energy Meter and GSM Prepaid Energy Meter. With the current technology, you need to go to the meter reading room and take down readings. Thus monitoring and keeping track records of your electricity consumption is a tedious task. To automate this, we can use the Internet of Things. The Internet of Things saves time and money by automating remote data collection. Smart Energy Meter has received quite a lot of acclaim across the globe in recent years. So, why not to build our own IoT Based Electricity Energy Meter?

We need to select the current sensor as well as the voltage sensor so that the current & voltage can be measured and thus we can know about the power consumption & total power consumed. The best current sensor available in the market is SCT-013. This is ***SCT-013** Non-Invasive AC Current Sensor Split Core Type Clamp Meter Sensor which can be used to measure AC current up to 100 amperes. Similarly, the best voltage sensor is the AC Voltage Sensor Module ZMPT101B. The ***ZMPT101B*** AC Voltage Sensor is the best where we need to measure the accurate AC voltage with a voltage transformer.

Using the SCT-013 Current Sensor & ZMPT101B Voltage Sensor, we can measure the all required parameters needed for Electricity Energy Meter. We will interface the SCT-013 Current Sensor & ZMPT101B Voltage Sensor with ***ESP32 Wifi Module*** & Send the data to Blynk Application. The Blynk Application Dashboard will display the Voltage, Current, Power & total unit consumed in kWh.

## Bill of Materials
The list of components required for making IoT Based Electricity Energy Meter are given below

| S.N. | Components                                 | Quantity | Buy From                                    |
|------|--------------------------------------------|----------|---------------------------------------------|
| 1    | ESP32 WiFi Module                          | 1        | [Amazon](https://amzn.eu/d/dFBzRPP) \|        
| 2    | ZMPT101B AC Voltage Sensor Module          | 1        | [Amazon](https://amzn.eu/d/9o1yY6f) \|      
| 3    |  Non-invasive AC Current Sensor | 1        | [Amazon](https://amzn.eu/d/8a2VHif) \|        
| 4    | 16x2 LCD Display                           | 1        | [Amazon](https://amzn.eu/d/7GPfwVa) \|   
| 5    | Potentiometer 10K                          | 1        | [Amazon](link) \|      
| 6    | Resistor 10K                               | 2        | [Amazon](link) \|   
| 7    | Resistor 100ohm                            | 1        | [Amazon](link) \|        
| 8    | Capacitor 10uF                             | 1        | [Amazon](link) \| 
| 9    | Connecting Wires                           | 10       | [Amazon](link) \|
| 10   | Breadboard                                 | 1        | [Amazon](link) \|    |


## SCT-013 Current Sensor

The SCT-013 is a Non-invasive AC Current Sensor Split Core Type Clamp Meter Sensor that can be used to measure AC current up to 100 amperes. Current transformers (CTs) are sensors are for measuring alternating current. They are particularly useful for measuring whole building electricity consumption. The SCT-013 current sensors can be clipped straight either to the live or neutral wire without having to do any high voltage electrical work.



Like any other transformer, a current transformer has a primary winding, a magnetic core, and a secondary winding. The secondary winding comprises many turns of fine wire housed within the casing of the transformer.



Specifications
1. Input Current: 0-30A AC
2. Output Signal: DC 0-1 V
3. Non-linearity: 2-3 %
4. Build-in sampling resistance (RL): 62 Ω
5. Turn Ratio: 1800:1
6. Resistance Grade: Grade B
7. Work Temperature: -25 °C~+70 °C
8. Dielectric Strength (between shell and output): 1000 V AC / 1 min 5 mA

## ZMPT101B AC Single Phase Voltage Sensor


The ZMPT101B AC Single Phase voltage sensor module is based on a high precision ZMPT101B voltage Transformer used to measure the accurate AC voltage with a voltage transformer. This is an ideal choice to measure the AC voltage using Arduino or ESP32.

The Modules can measure voltage within 250V AC voltage & the corresponding analog output can be adjusted. The module is simple to use and comes with a multi-turn trim potentiometer for adjusting and calibrating the ADC output.

Specifications
1. Voltage up to 250 volts can be measured
2. Lightweight with on-board micro-precision voltage transformer
3. High precision on-board op-amp circuit
4. Operating temperature : 40ºC ~ + 70ºC
5. Supply voltage 5 volts to 30 volts

You can use ZMPT101B for AC Voltage Monitoring applications.



## Circuit Diagram & Hardware Setup
Now let us see the circuit diagram of IoT Based Electricity Energy Meter using ESP32. The circuit has been designed using Fritzing software.

IoT Based Electricity Energy Meter

The connection diagram is simple. Both the Sensor, i.e. SCT-013 Current Sensor & ZMPT101B Voltage Sensor VCC is connected to Vin of ESP32 which is a 5V Supply. The GND pin of both the modules is connected to the GND of ESP32. The output analog pin of the ZMPT101B Voltage Sensor is connected to GPIO35 of ESP32. Similarly, the output analog pin of SCT-013 Current Sensor is connected to GPIO34 of ESP32. You need a two resistor of 10K & a single resistor of 100 ohms connected along with a 10uF Capacitor.

