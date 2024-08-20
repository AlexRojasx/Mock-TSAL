# Mock-TSAL
Will update soon with ideas and Schematics (haven't been able to update due to covid and summer camp voulnteering, will update soon) 🔥

<h2>Design constraints:</h2>

- must be controlled directly by the High Voltage, not programmed
- must turn on red light when voltage exceeds 60v
- must be able to handle much higher voltages as well
- when higher than 60v, must be Red Blinking at 2-5 Hz
- when lower than 60v, must be Solid Green
- Must Be illuminated when GLV (grounded Low Voltage) is activated

<h2>Current Ideas:</h2>

- create a voltage divider that works from 60v-600v tha goes to an Op amp comparator to send a signal to the lights
- after research into other TSAL circuits, alot of them use a voltage divider on the high voltage side to compare to a set referance on a Op amp Comparator, whose signal is sent to a Octo coupler for high voltage and low voltage isolation.
- for the referance voltage from the low side, i either need a isolated dc/dc converter or a second voltage divider on the high voltage side, though, in order to implement a second voltage divider I might need a dc/dc converter to drop the high voltage down. I will design the board initially with an isolated low voltage converter to supply the high voltage side comparator with a signal from the low voltage side.
<h2>Project Description:</h2>


<h2>Skills Learned:</h2>

-PCB Design and Layout  

<h2>Tools Used:</h2>

-Kicad for PCB Layout and Design  

<h2>Screenshots:</h2>

![image](https://github.com/user-attachments/assets/53b66dc4-b5dc-4191-a5d3-bac879c614e4)

For the Voltage divider cicuit I used a circuit simulator to confirm that the voltage and current were correct for my applications. I decided to use 1M ohms and 55k ohms as those values will give me a voltage of just above 3v when HV=60v and when HV=600v, it will be clamped at 12 v as there is a 12v zener diode clamping it.

![image](https://github.com/user-attachments/assets/8e7c4759-b41a-4caf-ac43-5b84c9aa569e)

The Op amp comparator is a LM311, the comparator and resistors on the imput are to help reduce noise coupling. This is detailed in the aplication notes (literature num: SNOA860) for the LM111,211,311 family of op amp comparators. The in+ is from the HV voltage divider so it should never be more than 12v, the in- is from a 3v referance voltage created from a voltage divider powered by an isolated 12v dc/dc converter powered by the low voltage on the pcb. On the imput voltage for the Op amp comparator, I placed a 0.1 uF decoupling capacitor to reduce any noise in the input voltage. The signal from the comparator is driving the octocoupler to send a high or low signal to the low voltage side of the PCB to drive the TSALs.

<h2>What Could be Improved:</h2>
