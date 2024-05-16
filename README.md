# VLSI-LAB-EXP-6
# SCHEMATIC ENTRY AND SIMULATION OF CMOS INVERTER, CMOS NAND and CMOS NOR USING CADENCE TOOL

**AIM:** To design and simulate the CMOS inverter and observe the DC and Transientresponse using cadence tool.

**APPARATUS REQUIRED:**  

Laptop with MobaXterm
Cadence tool

**PROCEDURE :**

1.Open Vivado: Launch Xilinx Vivado software on your computer.  

2.Create a New Project: Click on "Create Project" from the welcome page or navigate through "File"
> "Project" > "New".

3.Project Settings: Follow the prompts to set up your project. Specify the project name, location,
and select RTL project type.

4.Add Design Files: Add your Verilog design files to the project. You can do this by right-clicking on
"Design Sources" in the Sources window, then selecting "Add Sources". Choose your Verilog files
from the file browser.

5.Specify Simulation Settings: Go to "Simulation" > "Simulation Settings". Choose your simulation
language (Verilog in this case) and simulation tool (Vivado Simulator).

6.Run Simulation: Go to "Flow" > "Run Simulation" > "Run Behavioral Simulation". This will launch
the Vivado Simulator and compile your design for simulation.

7.Set Simulation Time: In the Vivado Simulator window, set the simulation time if it's not set
automatically. This determines how long the simulation will run.

8.Run Simulation: Start the simulation by clicking on the "Run" button in the simulation window.

9.View Results: After the simulation completes, you can view waveforms, debug signals, and analyze
the behavior of your design.

**SCHEMATIC ENTRY :**
 
**Creating a new library:**

1.In the library manager, execute File - New library. The new library form appears.

2.In the new library form, type ‘my design lib’ in the name section.

3.In the field of directory section, verify that the path to the library is set to ~/Database / Cadence-
analog – lab –bl3 and click ok.

4.In the next ‘technology file for new library form select option attach to an existing tech file and
click ok.

5.In the ‘attach design library to technology file’ form, select gpdk045 form the cyclic field and click
ok.

6.After creating a new library you can verify it from the library manager.

7.If you right click on the ‘my design lib’ and select properties, you will find that gpdk045 library is
attached as techlib to ‘my design lib’.

**Creating a schematic cell view :**

1.In the CIW or library manager, execute file – new – cell viw.

2.Setup the new file form as follows, Do not edit the library path file and the above might be
different from the path shown in your form.

3.Click ok when done the above setting. A black schematic window for the inverter design appears.

**Adding components to schematic:**

1.In the inverter schematic window, click the instance fixed menu icon to display the add instance
form.

2.Click on the browse button. This opens up a library browser from which you can select
components and the symbol view.

3.After you complete the add instance form move your cursor to the schematic window and click
left to place a component. LIBRARY NAME CELL NAME gpdk045 PMOS gpdk045 NMOS.

4.This is a table of components for building the inverter schematic.

5.After entering components, click cancel in the add instance form or press ESC with your cursor in
the schematic window.

![image](https://github.com/Logesh-KS/VLSI-LAB-EXP-6/assets/113246318/a91808f3-7396-4372-b8a7-cd6f16681a3c)


**Adding pins to schematic:**

1.Click the pin fixed menu icon in the schematic window. You can execute create pin or press ‘p’.

2.Add pin form appears. Type the following in the ADD pin form in the next order leaving space between the pin. PIN NAMES DIRECTION Vin,Vdd,Vss Input Vout Output.

3.Select cancel and then the schematic window enter window file or press the f bind key. 

**Adding wires to schematic:**

1.Click the wire (narrow) icon in the schematic window.

2.In the schematic window click on a pin of one of your components as the first point for your wiring. A diamond shape appears over the starting point of this wire.

3.Follow the prompts at the bottom of design window and click left on the destination point for your wire. A wire is routed between the source and destination points.

4.Complete the wiring as shown in the figure and when done wiring press ECS key in the schematic window to cancel wiring.

5.Saving the design: Click the check and save icon in the schematic editor window observe CIW output for any errors.

**BUILDING THE INVERTER TEST DESIGN: Creating the inverter test cell view:**

1.In the CIW or library manager, execute file – new – cell view.

2.Setup the newfile as shown below.

3.Click ok when done. A blank schematic window for the inverter test design appears.

4.Using the components list and properties/ comments in this table build the inverter test schematic. LIBRARY NAME CELL VIEW NAME PROPERTIES/COMMENTS My design lib Inverter Symbol Analog lib Vpulse Voltage1 = 0, Voltage2 = 1.8, delay Time = 0, Rise time=Fall time=1ns Period=20ns Analog lib Vdc, gnd Vdc = 1.8v.

5.Add the above components using create – instance or by pressing I.

6.Click the wire (narrow) icon and wire your schematic.

7.Click create wire name or press c to name the i/p (vsin) and output wires as in below schematic.

8.Click on the check and save icon to save the design.

![image](https://github.com/Logesh-KS/VLSI-LAB-EXP-6/assets/113246318/dbc9f50e-28de-426a-8a16-899267da9ecc)

**ANALOG SIMULATION WITH SPECTRA: Starting the simulation environment:**

1.In the Inverter-test schematic window execute launch – ADEL. The variable virtuoso analog design environment (ADE) simulation window appears. Choosing a simulator:

2.In the simulation window (ADE) execute setup – simulator / directory / host.

3.In the choosing simulator form, set the simulator field to specra and click ok.

4.In the simulation window (ADE) execute the setup model libraries. To complete, move the cursor and click ok. 

**Choosing Analysis:**

1.Click the choose- Analysis icon in the simulation window (ADE). 

2.The choosing analysis form appears.

3.To Setup the transient analysis. a. In the analysis section select tron. b. Set the stop time as 100ns c. Click at the moderate or enabled button and the bottom and then click apply.

4.To set for DC analysis a. In the analysis section select DC. b. Turn on save DC operating point. c. Turn on the component parameters. d. Double click the select Vpulse source or Type V0 (capital V zero). e. 

5.Select the DC voltage in the select window parameter and click in the form start and stop voltages are 0 to 1.8. f. Select the enable button and click apply and then click ok.

**Selecting output for plotting:**

1.Execute the o/p’s to be plotted -select on sschematic in the simulation window.

2.Follow the prompt at the bottom. Click on the o/p net vout input vin of the inverter. Press esc with the cursor after selecting.

**Running the simulation:**

1.Execute the simulation Netlist and run in the simulation window to start the simulation on the icon. This will create the netlist as well as run the simulation.

2.When the simulation finishes the transient and DC plots automatically will be popped up along with netlist.

![image](https://github.com/Logesh-KS/VLSI-LAB-EXP-6/assets/113246318/b339a0eb-c6e3-46ca-9c49-ce614efcc100)

![image](https://github.com/Logesh-KS/VLSI-LAB-EXP-6/assets/113246318/451241a0-510e-450c-99dd-035eb6b7f500)

**CMOS NAND GATE**

**NAND SCHEMATIC**

![image](https://github.com/Logesh-KS/VLSI-LAB-EXP-6/assets/113246318/18c63cf5-417f-46fc-a3a5-330847007bbb)

**NAND TEST CELL VIEW**

![image](https://github.com/Logesh-KS/VLSI-LAB-EXP-6/assets/113246318/07bea821-9212-4fb4-aa28-2f6eb33d8afb)

**NAND SIMULATION WITH SPECTRA**

![image](https://github.com/Logesh-KS/VLSI-LAB-EXP-6/assets/113246318/5413e719-3c98-48db-ac28-bdd7ab4b24af)

**CMOS NOR GATE**

**NOR SCHEMATIC**

![image](https://github.com/Logesh-KS/VLSI-LAB-EXP-6/assets/113246318/5f9d8371-12be-43af-bfd4-afa2134627a7)


**NOR TEST CELL VIEW**

![image](https://github.com/Logesh-KS/VLSI-LAB-EXP-6/assets/113246318/dbf37cf9-b089-419f-8e46-6da0b7a3cbca)

**NOR SIMULATION WITH SPECTRA**

![image](https://github.com/Logesh-KS/VLSI-LAB-EXP-6/assets/113246318/d99caea3-4bdf-4467-9f0f-bb0de8e2e96b)

**RESULT:** THe design and simulation of the CMOS inverter and the DC and transient responses using cadence tool is successfully observed and verified.









