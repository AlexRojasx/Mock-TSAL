# Mock-TSAL
Will update soon with ideas and Schematics  🔥

<h2>Design constraints:</h2>

- must be controlled directly by the High Voltage, not programmed
- must turn on red light when voltage exceeds 60v
- must be able to handle much higher voltages as well
- when higher than 60v, must be Red Blinking at 2-5 Hz
- when lower than 60v, must be Solid Green
- Must Be illuminated when GLV (grounded Low Voltage) is activated

<h2>Current Ideas:</h2>

- create a voltage divider that works from 60v-600v tha goes to a comparator to send a signal to the lights
- after research into other TSAL circuits, alot of them use a voltage divider on the high voltage side to compare to a set referance on a Op amp Comparator or other comparator, whose signal is sent to a Octo coupler for high voltage and low voltage isolation.
- for the referance voltage from the low side, i either need a isolated dc/dc converter or a second voltage divider on the high voltage side, though, in order to implement a second voltage divider I might need a dc/dc converter to drop the high voltage down. I will design the board initially with an isolated low voltage converter to supply the high voltage side comparator with a signal from the low voltage side.
<h2>Project Description:</h2>


<h2>Skills Learned:</h2>

-PCB Design and Layout  

<h2>Tools Used:</h2>

-Kicad for PCB Layout and Design  

<h2>Screenshots:</h2>


<h2>What Could be Improved:</h2>
