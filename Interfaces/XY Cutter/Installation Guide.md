# For Download Interface Click the button

# I**ntroduction**

[Untitled video - Made with Clipchamp (17).mp4](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/8d0c6533-70be-477b-9e03-fbc4182dc330/Untitled_video_-_Made_with_Clipchamp_(17).mp4)

CNC cutting machines are typically designed for cutting two-dimensional designs and include two axes, X and Y, used for cutting materials such as metal, wood, plastic, and others. These machines may also feature a Z axis, which adjusts the cutting nozzle's distance from the workpiece surface. However, the Z-axis control in these machines is usually not automated or performed via G-Code; instead, the operator must manually adjust the nozzle's distance. The Z-axis motors can be AC, DC, stepper, or servo motors, and depending on the type and thickness of the materials, the cutting nozzle can be equipped with air gas, plasma, waterjet, laser, etc.

---

## **Radonix Interfaces for CNC Cutting Machines**

Radonix, a manufacturer of CNC controllers, has thoroughly analyzed these types of machines and designed dedicated interfaces for them. The **XY-Cutter** and **XYZ-Cutter** interfaces are specifically designed for these machines:

- **XY-Cutter Interface**: For machines without a Z-axis or with AC and DC motors for the Z-axis.
- **XYZ-Cutter Interface**: For machines with a Z-axis and stepper or servo motors.

In these interfaces, all inputs, outputs, and functions are designated with the prefix **C-**.

**Key Features of Radonix Interfaces**

- Direct execution of design files without the need for conversion to G-Code.
- The ability to select individual parts from a large file and define the sequence and direction of cutting for each piece.
- Design editing in the software with features such as Scale, Rotate, and Flip.
- Software-based correction of workpiece misalignment, especially for heavy sheets.
- Separate pauses for before, during, and after cutting.
- Reverse execution of designs and the ability to run demos without activating the cutting output.
- Execution of 2D designs on cylindrical surfaces such as pipes.

These features enable Radonix interfaces to provide more precise control and greater efficiency in the cutting process.

<aside>
❗

**This interface is called XY Cutter** 

</aside>

Radonix provides **three distinct interfaces** for **XY Cutter machines**, categorized based on the strategy and functionality of the **Z Axis**. This division ensures compatibility with various machine types and operational requirements. Below is a detailed explanation of these interfaces:

### **1. XY Cutter Interface (DC Motor-Controlled Z Axis)**

The **XY Cutter** interface is designed for machines using **DC motors** to control the Z Axis. In this setup:

- The Z Axis is controlled via output links:
    - **C-Zfree,1** for upward movement.
    - **C-Zfree,-1** for downward movement.

This simple control method does not involve pulse and direction signals, making it suitable for basic XY cutting machines. Operators can activate the outputs to move the Z Axis up or down as required.

---

### **2. XYZ Cutter Interface (Manual Stepper/Servo-Controlled Z Axis)**

The **XYZ Cutter** interface is intended for machines using **stepper or servo motors** in **manual mode**. In this configuration:

- The Z Axis is controlled via **pulse and direction signals**, directly connecting to the **Axis control pins**.
- Operators can manually adjust the Z Axis position **during toolpath execution** to ensure the cutting tool (e.g., plasma torch) maintains the correct height from the workpiece surface.

This interface is particularly suited for applications where manual intervention is required to maintain precision during operation.

---

### **3. XYZ Cutter + THC Interface (Automatic Stepper/Servo-Controlled Z Axis)**

The **XYZ Cutter + THC** interface is designed for machines where the Z Axis operates in **automatic mode**, managed by the **THC (Torch Height Control)** module. This configuration relies on feedback from the plasma unit's arc voltage:

- **Feedback Voltage Control:**
    - As the plasma arc length increases, the **feedback voltage** from the plasma unit rises.
    - Conversely, as the arc length decreases, the feedback voltage drops.
- **Automatic Adjustment:**
    - The Z Axis dynamically adjusts its height based on the feedback voltage to maintain the optimal cutting distance.

The **THC module** ensures real-time adjustments, providing consistent and precise cutting performance. This interface is ideal for high-precision plasma cutting machines where automatic height control is critical.

---

## **Summary**

**Radonix's** interfaces for XY Cutter machines are tailored to meet various operational needs:

1. **XY Cutter Interface:** For basic machines with DC motor-controlled Z Axis, using **C-Zfree,1** and **C-Zfree,-1** outputs for up/down movement.
2. **XYZ Cutter Interface:** For stepper/servo motors with manual operator control of the Z Axis via pulse and direction signals.
3. **XYZ Cutter + THC Interface:** For stepper/servo motors with plasma arc feedback, dynamically managed by the **Torch Height Control (THC)** module.

These interfaces ensure Radonix controllers provide versatility, precision, and adaptability for a wide range of cutting applications.

---

<aside>
❗

For starting primary installation there are some steps to go throw it and has a successful installing

</aside>

# Get Start

## Workspace Descriptions

1- Study about different part of interface which is named and indicated in photo it means that you should get familiar with all elements like Buttons , screen , bars , volume , values , … anything on interface you have accesses 

![Image](https://github.com/user-attachments/assets/08521506-983e-4f7b-b2ac-f8d03c0f210e)

![Image](https://github.com/user-attachments/assets/8f79758e-caae-4704-a0ef-c0e4ec820220)

---

### **Top Status Bar**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/86b07580-1228-4cff-964c-af8dd919d552/image.png)

- **Online** (Yellow Light): Indicates the machine's connection status. Yellow may mean a standby mode or that it's not fully online.
- **X Axis, Y Axis,**  (Green Lights): These lights show the operational status of each axis. Green typically means these axes are active or ready.
- **Alarm, Emergency** (Brown Lights): Indicators for critical safety statuses. When activated, they may change color (e.g., red) to signal an alarm, emergency stop.

---

### **Position and Speed Readouts (Right Panel)**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/832cbe24-a996-4561-b126-692bceab3881/image.png)

- **Position** :

This position is shown based on where the reference point has been selected. 

- **Velocity** (Below Relative Position): Shows the current operational speed in mm/s, useful for monitoring real-time cutting or movement speeds.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/dc358b23-0b6f-4df9-a3f0-2806703dd02f/image.png)

---

### **Real-Time Reference Adjustment in Radonix Interfaces**

Radonix interfaces offer a **dynamic reference adjustment feature**, allowing operators to redefine the reference point at any moment during the operation. This feature enhances flexibility and precision in workflows, making it suitable for diverse applications.

it means that operator can change start point of workpiece on the table. 

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/b817db5e-69a1-41b1-89cd-c4abde47e3f6/image.png)

- Cut Velocity : This parameter defines the velocity of cut .

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/30ad1300-f392-4471-9472-6b0f07955316/image.png)

- **Manual Jogging Controls** :
    - **Arrows** (X+, X-, Y+, Y-): These buttons manually jog the machine along the X and Y axes, allowing for precise positioning adjustments by moving the tool head incrementally.

You can switch the jog mode by pressing this button according fig 01-05  and it will change to figure 01-06, changing from continuous to incremental movement. This means you can define a value in this section according fig 01-07 which has been indicated in red area , and after pressing the coordinate axis jog, the axis will move by the amount you have entered.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/520d9e21-7969-4221-af56-e738c288eb52/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/a2899a09-3ae6-4d6f-913f-dbf2f3dfd682/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/99c1a585-6b60-4dfc-ad18-b92fca03545d/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/628f1052-e618-4a96-be08-e65a07eef1b3/image.png)

---

### **Feed Rate and Tool Parameters (Lower Right Panel)**

- **V (mm/s)** and Step**(mm)**: Input fields for setting feed rates and movement limits along each axis. "V" controls the velocity (or speed) in mm/s, and "L" could define the step size for each manual jog.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/7649f0f8-4c0d-49dd-98e7-2d8413e740f1/image.png)

- **Scroll**  (Vertical Slider on Bottom Right ):According to figure 01-08 which is demarcated with red area or  Allows for real-time adjustment of the feed rate or speed as a percentage. This control can quickly change the speed without directly altering program values.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/0fe94eda-6670-4bb4-97c5-ec817e4e45f1/image.png)

---

### **Main Program Controls**

- **Settings (Gear Icon)**: Opens the configuration menu, where detailed settings for the CNC machine can be adjusted.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/01bb0d3a-3f27-41e4-ba99-d9909511dc6a/image.png)

- The Exit icon allows you to close the program
- The Minus icon lets you minimize it.
- The $ icon create  a report  from the workpiece and operator can estimate the price

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/7dde4bf3-ec65-4f49-a635-8e13a03ac9d1/image.png)

---

### **Interface specification**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/4a4b9fa4-3469-43a5-a338-ef10f0914f2d/image.png)

This section of the interface displays the current status and features of the system. It also updates to show alarms and processes every second. For a detailed report, double-click on this section.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/8d50447e-feab-4fbf-a208-d1a3b444d766/image.png)

---

### **Main Program Controls (Bottom Center)**

- **Open File** (Folder Icon): Opens a file dialog for loading a CAM (Computer-Aided Manufacturing) file, typically a G-code  or DXF program.

---

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/93126732-0b77-488e-9372-1171645d5698/image.png)

This section is dedicated to controlling G-Code execution:

- **RUN**: This button starts the G-Code process.
- Backward: 
The **Backward** button provides operators the ability to step back within the G-Code toolpath execution process. This feature is essential for troubleshooting, rechecking, or re-executing specific portions of the G-Code.
- **Pause**: This button halts the toolpath.
- **Reset**: This button resets the toolpath.

# ~~Relations Between Outputs and Inputs~~

# Inports

In this section, we will examine the configuration of the Inputs.

Essentially, when the Inports branch is opened, these settings will appear.

**Setting Up Inputs: General Overview**

Configuring inputs in our CNC system is an essential step to ensure smooth operation, precise control, and safety. Inputs can be categorized into two main types based on their configuration and purpose: **Hardware-Based Inputs** and **Software-Based Inputs.** This flexibility allows the system to adapt to a wide range of applications and machine requirements.

---

## **1. Hardware-Based Inputs**

Hardware inputs involve physical devices connected to the controller, enabling direct interaction with the machine's environment. These inputs are crucial for safety, machine control, and real-time feedback.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/b6bf2353-d2c8-46e5-b817-7852a26c6ed7/image.png)

The digital inputs of Radonix controllers are named as I.[n], where n is a number greater than zero and represents the input number. These inputs are isolated by optical couplers and have low noise tolerance due to their low impedance.

The digital inputs on Radonix controllers have the capability to switch between NPN and PNP modes depending on the output of the device or sensor. The mode changeover switch must be set to PNP position for devices with PNP output and NPN position for devices with NPN output.

In various branches of industrial automation, there are equivalent terms for PNP and NPN. Some
examples of these terms include:
NPN = Sink = Low Active
PNP = Source = High Active

---

**Switching Between PNP and NPN Modes in Radonix Systems**

The ability to switch between **PNP** (positive logic) and **NPN** (negative logic) modes in Radonix controllers depends on the specific **board model** being used. This flexibility allows the system to be compatible with different wiring and sensor configurations.

- **PC Pro LAN:**
    - A **small DIP switch** is present on the board.
    - This switch allows users to toggle between **PNP** and **NPN** modes.
    - **How to Use:**
        - Locate the DIP switch on the board.
        - Toggle the switch to the desired mode (PNP or NPN).
        - Ensure the board is powered off before making changes to prevent damage.
            
            ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/5234e53a-523b-434b-be9f-d99db25f2795/image.png)
            
        
- **PC Smart:**
    - Instead of a DIP switch, the **PC Smart** model uses a **Come Pin** for each set of 4 input pins.
    - This pin allows you to define the input logic (PNP or NPN) for the corresponding inputs.
    - **How to Use:**
        - Connect the **Come Pin** to the appropriate voltage (positive for PNP or ground for NPN).
            
            **1.PNP Mode (Source Mode):**
            
            - If the COM pin is connected to **0V**, the input pins will be triggered (turned ON) by a **24V signal**.
                - In this configuration, the sensor’s output wire must provide a 24V signal to activate the input.
            
            **2.NPN Mode (Sink Mode):**
            
            - If the COM pin is connected to **24V**, the input pins will be triggered (turned ON) by a **0V signal**.
                - In this configuration, the sensor’s output wire must pull the input to 0V to activate it.
        - Each group of 4 input pins has its own Come Pin, allowing for mixed configurations within the same board.
        
        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/ba60d093-16bc-4c0e-aa31-cc53ea55edea/image.png)
        

**Examples of Hardware Inputs:**

- **Limit Switches:** Define physical boundaries for axis movement.
- **Home Sensors:** Establish the reference (Home) position for the machine most of them are **Proximity**
- **Emergency Stop Buttons:** Ensure immediate halting of operations in emergencies.
- **Other Proximity Sensors:** Detect objects or tools in the machine's workspace.
- **Push Buttons and Selector Switches:** Trigger specific machine functions or modes.
- **Scanners:** Measure or detect specific properties, often used in specialized processes such as Glass **or gold CNC operations**.

**Configuration Process:**

1. **Connection:** Physically connect the hardware component (e.g., a switch or sensor) to the designated input pin on the controller.
2. **Input Definition:** Use the controller software to define the role of the input (e.g., `HomePin`, `LimitPin`, or a custom input for specific functions).
3. **Polarity Settings:**
    - Set the input type as **Normally Open (NO)** or **Normally Closed (NC)** based on the connected hardware's default state.
    - For example:
        - An NC emergency stop button remains active (closed) until pressed.
        - An NO proximity sensor activates (closes) only when an object is detected.

---

## **2. Software-Based Inputs**

**Software-Based Inputs** provide simple logical functionality to configure arbitrary links and integrate them with related physical hardware .They facilitate quick and simple installation without the need for microprogramming. Users can simply select options from a list and configure settings to maximize efficiency.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/4bc60a0b-b42f-4c30-9f75-4b33a0192ea7/image.png)

As illustrated in the figure, each input is divided into three sub-branches, as detailed below:

1. **Enable**: This sub-branch can be set to two values: True or False.
2. **Link**: Specifies the duty or task that needs to be performed or checked. This includes any device that can serve as an input, such as sensors, buttons, and switches.
3. **NC**: Determines whether the specific input is Normally Open (NO) or Normally Closed (NC).

**Examples of Software Inputs:**

- **Virtual Limit Switches:**
    - Use software parameters to define axis movement boundaries based on the machine's table size.
- **Logical Triggers:** Define conditional triggers for specific operations (e.g., When the axis reaches the limit switch ).
- **Simulated Inputs:** Use for testing or scenarios where physical components are unavailable.

**Configuration Process:**

1. **Access Configuration Interface:**
    - Open the controller's software settings to manage inputs.
2. **Define Parameters:**

        As an example to set  limit Switch : 

- setting —→ System —→ In ports —→ Enabled= True

                                                                                Linked = LimitPin,X

                                                                                 NC= True

- Configure additional logical conditions for interlocks or simulations.
1. **Validate Settings:**
    - Test the software by CAM Pro TEST  input configurations to ensure proper functionality and safety.

---

# Outputs

In this section, we will examine the configuration of the Outputs.

**Setting Up Inputs: General Overview**

In Radonix systems, **Outports** are critical components that manage the output signals controlling various peripherals, such as relays, actuators, alarms, and other devices. Outputs can be categorized into two main types based on their configuration and purpose: **Hardware-Based Inputs** and **Software-Based outputs.**
This flexibility allows the system to adapt to a wide range of applications and machine requirements.

## **1. Hardware-Based Outputs**

Hardware outputs involve physical signals sent from the controller to external devices, enabling direct control of the machine’s environment. These outputs are critical for operational safety, machine actuation, and real-time command execution, ensuring efficient workflow and coordination within the CNC system.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/0272e6ad-833a-4b06-9733-bc681e5375dd/image.png)

The digital outputs of Radonix controllers are named O.[n], where n is a numerical identifier greater than zero and represents the output number .

Radonix controllers incorporate robust protection mechanisms for **Outports** to ensure durability, safety, and reliability. These mechanisms vary between different models, specifically the **PC-Pro** and **PC-Smart** boards, each with distinct protection features and failure handling processes.

### **Output Behavior in PC-Pro LAN Models**

- The **PC-Pro LAN** model outputs are fixed in **NPN mode**.
- **How It Works:**
    - When an output is **ON**, it provides **0 volts** by pulling the signal to ground.
    - When an output is **OFF**, it is in a high-impedance state, effectively disconnecting the circuit.
- **Wiring Consideration:**
    - Connected devices must be compatible with NPN logic, where the load receives voltage from a positive source and is activated when the output pulls the circuit to ground.
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/3a3aca22-7fd6-4428-b66c-19b01731118a/image.png)
    

### **Output Behavior in PC-Smart Models**

- The **PC-Smart** model offers a flexible configuration where outputs can operate in **PNP mode** or **NPN mode**, depending on the connection of the **COM Pin**.
- **How It Works:**
    - The voltage provided by the outputs depends on what is connected to the **COM Pin**:
        - **COM Pin Connected to 24V:** Outputs will provide **24 volts** when activated.
        - **COM Pin Connected to Ground:** Outputs will provide **0 volts** when activated (NPN mode).
- **Flexibility:**
    - This design allows PC-Smart models to adapt to different wiring requirements and device logic preferences.
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/455205eb-8c3c-4cd8-815d-b73826fbc9e6/image.png)
    

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/50ea19ad-9754-4df1-ab4a-9e36161d058d/image.png)

**Configuration Process for Outputs:**

1. **Connection:**
    - Physically connect the hardware component (e.g., relay, electric valve , Barke , alarm) to the designated output pin on the controller.
    - Ensure proper wiring based on the required logic (PNP or NPN) and voltage compatibility.
2. **Output Definition:**
    - Use the controller software to define the role of the output (e.g., `C-CutPin`, `Brake`, or a custom output for specific functions).
    - Assign the output to its intended device or operation in the system settings.
3. **Logic Settings:**
    - Set the output logic based on the connected device's requirements:
        - **Active High (PNP):** The output sends voltage (e.g., 24V) when activated.
        - **Active Low (NPN):** The output pulls the signal to ground (0V) when activated.
4. **Testing and Validation:**
    - After configuring, test the output to ensure it operates as intended in CAM Pro Test application.
    - Use a multimeter or other diagnostic tools to verify output voltage and behavior.

## **2. Software-Based Outputs**

**Software-Based Outputs** provide simple logical functionality to configure and integrate them with related physical hardware. These features are crucial for enhancing control capabilities. They facilitate quick and simple installation without the need for microprogramming. Users can simply select options from a list and configure settings to maximize efficiency.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/7e1544ec-505a-4cc3-acb7-acefbec970e4/image.png)

As illustrated in the figure, each output is divided into three sub-branches, as detailed below:

1. **Enable**: This sub-branch can be set to two values: True or False.
2. **Link**: Specifies the duty or task that needs to be performed or checked. This includes any device that can serve as an output, such as actuators, lights, and alarms.
3. **NC**: Determines whether the specific output is Normally Open (NO) or Normally Closed (NC).

**Examples of Software Outputs:**

- **Virtual Relays:**
    - Use software parameters to define activation boundaries for devices based on operational needs.
- **Logical Triggers:** Define conditional triggers for activating specific outputs (e.g.,  alarms or Relay for specific function  ).
- **Simulated Outputs:** Employ these for testing or in scenarios where physical components are not available.

**Configuration Process:**

1. **Access the Configuration Interface:**
    - Navigate to the controller's software settings to manage outputs.
2. **Define Parameters:**
    - To configure an output like an order to forward the VFD, enter parameters.
    - setting —→ System —→ Outports —→ Enabled= True
    
                                                                                     Linked = C-CutPin
    
                                                                                     NC= True
    
3. **Validate Settings:**
    - Test the configured software outputs to ensure they function correctly and safely, verifying their effectiveness in real-world applications.

# **Setting Up Inputs: Simple and Intuitive Configuration**

In Radonix system, configuring inputs or Outputs  is designed to be as user-friendly as possible, without requiring any microprogramming or advanced technical knowledge. All you need to do is navigate to the **Inputs** section of the controller interface, open the settings drawer, and select the item you need to configure. The same process applies to other sections, such as **Outputs** or any other functional areas.

### **Step-by-Step Configuration Process**

1. **Access the Desired Section:**
    - Go to the section you want to configure, such as **Inputs** or **Outputs**, depending on the functionality you are setting up.
2. **Open the Settings Drawer:**
    - Within the selected section, locate the specific input branch or subsection.
    - Click or expand the settings drawer to reveal the available options.
3. **Select the Required Item:**
    - Choose the input type or functionality you want to configure (e.g., limit switch, home sensor, emergency stop, or custom inputs).
    - Define the specific role for the input, such as `C-ZFreePin,1`
4. **Set Parameters Easily:**
    - Adjust the necessary parameters, such as polarity (Normally Open or Normally Closed), response delays, or logical behavior, directly from the interface.
5. **Save and Test:**
    - Save your settings and validate them through the controller interface to ensure everything is functioning as intended.
    - **In the end in order to finalizing you have to close program to save everything**

---

---

# **Installation and Setup Process for Radonix CNC Controller**

Radonix recommends following this detailed step-by-step guide for installing and configuring a Radonix CNC controller. The process encompasses everything from wiring the hardware to setting parameters in the software. This approach aims to guarantee a seamless installation experience for customers, addressing all critical components.

## **Wiring Components for a Radonix CNC Controller**

Proper wiring is the foundation of a reliable and high-performing CNC machine. A professional approach to wiring ensures seamless communication between the Radonix controller, servo or stepper motors, sensors, VFDs (Variable Frequency Drives), and other peripherals. This guide provides expert advice on wiring all components, including selecting appropriate power supplies, ensuring safety, and achieving optimal performance.

**1. Main Components Overview**

A typical CNC system includes the following components, all of which require precise and secure wiring:

1. **Radonix CNC Controller:** The central control unit.
2. **Servo or Stepper Motors:** Responsible for axis movement.
3. **Variable Frequency Drive (VFD):** Controls the spindle motor.
4. **Sensors:**
    - **Home Sensors** for axis referencing.
    - **Limit Switches** for boundary control.
- **Home Sensors** for axis referencing.
- **Limit Switches** for boundary control.
1. **Emergency Stop (E-Stop):** Ensures immediate shutdown during emergencies.
2. **Power Supplies:** Provides regulated power for different components.
3. **Peripheral Outputs:** Includes relays, coolant pumps, and alarms.

**2. Wiring the Main Power Supply**

**Choosing the suitable Power Supply**

- **Controller Power Supply:**
    
    It is recommended to use 24V switching power supplies to power the Radonix controllers. Calculating Power Supply Current To determine the required power supply current in the electrical panel, the current consumption of each element connected to the power supply must be calculated. For example, if there are 4 relays, 3 pneumatic solenoid valves, and a controller in a switchboard, the current consumption can be determined using Ohm’s law (V=I*R). The electric currents should be calculated and their sum considered as the current of the power supply, along with a confidence factor of a few percent. For example, if the current consumption of the relays is 0.1A and that of the solenoid valves is 0.25A, the total current can be calculated as follows: Total current = controller current + relay current + solenoid valve current IT = 0.5 + 4 * 0.1 + 3 * 0.25 = 1.65A
    

**3. Anti-Noise Measures for CNC Wiring**

Electromagnetic interference (EMI) or electrical noise is a common issue in CNC systems, particularly when wiring sensitive components like controllers, servo drives, and sensors. Noise can disrupt signals, cause erratic machine behavior, and even damage components over time. Implementing robust **anti-noise measures** is critical for ensuring the reliable and precise operation of your CNC machine.

**Sources of Electrical Noise**

1. **High-Frequency Devices:**
    - Variable Frequency Drives (VFDs)-  (In Related Machines)
    - Switching power supplies
2. **High-Power Components:**
    - Spindle motors - (In Related Machines )
    - Servo and stepper motors
3. **Long Cables:**
    - Longer cables act as antennas, picking up EMI.
4. **Proximity to Power Lines:** 
    - Signal and power cables running close together can cause interference.

**Key Anti-Noise Measures**

**1. Use Shielded Cables**

- **Purpose:** Shielded cables reduce the effect of electromagnetic interference on sensitive signals.
- **Implementation:**
    - Use twisted-pair shielded cables for signal lines like **Pulse+, Pulse-, Direction+, Direction-**, and sensor signals.
    - Connect the shield to ground at **one end only** to avoid ground loops.

**2. Separate Signal and Power Cables**

- **Purpose:** Prevent high-power cables from inducing noise in low-power signal cables.
- **Implementation:**
    - Route signal cables (e.g., sensor and control signals) separately from power cables (e.g., motor power and VFD output).
    - Maintain at least 10-15 cm of separation between these cable types.
    - Use different cable trays or conduits for power and signal lines.

**3. Proper Grounding**

- **Purpose:** A well-designed grounding system minimizes noise and protects components.
- **Implementation:**
    - Create a central grounding point in the electrical box, often referred to as a **grounding bus bar**.
    - Ensure all grounding wires (controller, drives, motors, etc.) connect to this central point.
    - Avoid daisy-chaining ground connections, which can introduce noise.

**4. Install Ferrite Beads**

- **Purpose:** Ferrite beads filter out high-frequency noise on signal and power cables.
- **Implementation:**
    - Clip ferrite beads onto signal and control cables near the controller or servo drives.
    - Use multiple beads for particularly noisy environments.

**5. Proper VFD Wiring**

- **Purpose:** VFDs are a significant source of electrical noise and require special attention.
- **Implementation:**
    - Use shielded cables between the VFD and spindle motor.
    - Ground the cable shield at the VFD end.
    - Install line filters or chokes on the VFD input and output to suppress noise.

**6. Shorten Cable Lengths**

- **Purpose:** Longer cables are more susceptible to picking up noise.
- **Implementation:**
    - Keep cable lengths as short as possible without compromising flexibility.
    - Avoid unnecessary slack or loops in the wiring.

**7. Use Isolated Power Supplies**

- **Purpose:** Prevent noise from one system affecting another.
- **Implementation:**
    - Use separate, isolated power supplies for sensitive components like sensors, encoders, and the controller.
    - Ensure power supplies are adequately rated and properly grounded.

**8. Use Optical Isolation**

- **Purpose:** Protect the controller from noise on external connections.
- **Implementation:**
    - Use opto-isolators for connections to external devices like sensors, relays, or switches.
    - Many Radonix controllers have built-in optical isolation for inputs and outputs.

**9. Secure Connections**

- **Purpose:** Loose connections can act as noise sources.
- **Implementation:**
    - Check all connectors for tight and secure connections.
    - Use locking connectors where possible to prevent accidental disconnections.

**10. Line Filters and Surge Protectors**

- **Purpose:** Suppress high-frequency noise and protect against voltage spikes.
- **Implementation:**
    - Install EMI line filters on the AC mains supply.
    - Use surge protectors on power inputs to the controller and VFD.

## **Software Configuration: Bringing the System to Life**

**Step 1: Install Radonix Cam Pro**

- Download and install the software on your PC.
- Upon turning on the controller, observe the LEDs on the LAN port: one should remain steady, while the other blinks.
- Connect the Radonix controller to the computer via a LAN or USB cable.

**Step 2: Initial Setup**

- Open the software and initialize the system.
- Perform a factory reset to ensure default settings are applied.

**Step 3: Configure Inputs**

- Navigate to **Settings > System > Inports.**
- Assign roles to each input:
    - `EmergencyStop` for the E-Stop button.
    - `HomePin, X/Y/Z` for home sensors.
    - `LimitPin, X/-X` for limit switches.
- Test each input by activating it physically and observing the software response.

**Step 4: Configure Outputs**

- Navigate to **Settings > System > Outports.**
- Assign roles to each output:
    - `C-CutPin` for turn on torch.
    - `C-ZfreePin,1` for active a Relay to move axis Z upward .
    - `C-ZfreePin,-1` for active a Relay to move axis Z downward .
- Test outputs by toggling them in the software and observing the connected devices.

**Step 5: Axis Calibration**

- Go to **Settings > System > Calibration.**
- Enter parameters for each axis:
    - **Steps per Unit:** Based on lead screw pitch, motor steps, and encoder resolution.
    - **Max Travel:** Define the maximum travel distance for each axis.
- Test calibration by commanding movements and measuring actual travel distances.

---

### **Emergency Stop (E-Stop)**

A critical response mechanism in industrial settings used to halt machinery and equipment immediately in order to protect against imminent danger. This action is typically engaged through an emergency stop button or switch that, when activated, interrupts the power supply and ceases all operations, effectively minimizing the risk of accidents, injuries, or damage to the machinery and personnel.

 **Configurable Emergency Mode:** 

An advanced feature in control systems that allows users to define and set up custom emergency responses through the system settings. This mode can be programmed to engage different levels or types of responses depending on the nature and severity of the threat detected.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/4d9b54ca-d964-4c44-a4e3-9be245e67591/image.png)

This variable is used to determine the operation that occurs when the Emergency button is pressed.

**Emergency Type** 

- **None**: When this mode is selected, the machine operation is similar to a pause. The device stops all activities but cannot be resumed from the same point if this mode is triggered.
- **ClearOutPorts**: Activating this mode stops the axes and turns off all digital output ports of the controller. This ensures that no further commands affect the machine's operation until reset.
- **ClearAnalog**: This mode stops the axes and turns off all analog outputs. It's used to ensure that any variable outputs controlling aspects like tool pressure or spindle speed are deactivated.
- **DisableAxes**: In this emergency mode, the axes of the machine are stopped and become inactive, which means the motors that drive the axes are disengaged, allowing them to move freely if manually pushed but not under power.
- **ResetToolPath**: This mode stops the axes and resets the toolpath to the start of the program. This is useful in scenarios where the process needs to be started from the beginning, either to prevent damage or to correct an error.
- **ClearOutPorts+ClearAnalog**: This comprehensive emergency mode combines the effects of ClearOutPorts and ClearAnalog, stopping all digital and analog outputs, disabling the axes, freeing the motors, and resetting the toolpath to the first coordinate. This is effectively a full reset of the system's operating state.
- **All**: Selecting "All" activates all the above emergency responses, providing the maximum level of immediate system shutdown. All outputs, both digital and analog, are turned off; axes are stopped and freed; and the toolpath is reset.

### **Home Sensors**

Home sensors are so crucial for positions it means that thanks to these sensors the position become meaningful ,  they are impact in defining table size  the sensors are machine zero point or machine origin point when axis reach the sensors the controller detect them and it causes that a red table is created in Black Grid space  so with this option each point in this area has its own position than sensors ın each axis  

Indeed, home sensors are integral to the function and accuracy of CNC machines. Let's explore further how these sensors interact with the CNC controller and influence the machine workspace setup:

**Role and Functionality of Home Sensors:**

1. **Defining the Origin:** Home sensors establish the machine's zero point or origin. This point serves as the reference for all other positions within the machine's operational space. It ensures that the machine knows the starting point for all axes (typically labeled X, Y, and Z).
2. **Impact on Table Size and Work Area Definition:** The detection of the home position by these sensors directly impacts the definition of the machine’s table size. This is because the machine controller uses the origin point to calculate and define the extents of the machine’s operational area or table. The movements and operations of the machine are confined within these calculated boundaries to ensure precision and to prevent the machine from moving beyond its capable limits, which could cause damage or errors.
3. **Visualization on Controller Interface:** When the home sensors are triggered, the CNC controller can visually depict this on its interface, often illustrated as a "red table" laid out on a "black grid" background. This visual representation helps operators to see and understand the active working area of the machine. It shows where tools can safely travel and operate, providing a clear demarcation of the workspace.
4. **Positional Accuracy:** Each point within this defined red table area has a specific position relative to the machine’s origin point, determined by the home sensors on each axis. This arrangement allows for precise control over the machine's movements and operations, ensuring that every motion made by the machine is accurately accounted for relative to the origin, enhancing both the precision and reliability of the work performed.
5. **Operational Reliability:** Regularly using home sensors to reestablish the machine’s origin point helps maintain operational accuracy and reliability, crucial for long-term consistent output, especially in precision-dependent applications.

Overall, home sensors not only provide a safety mechanism by defining the limits of machine operation but also enhance operational precision by establishing a clear and reliable reference point for all machining tasks. This setup ensures that every point within the operational area is accurately positioned relative to the origin, making the machine's functioning both predictable and precise.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/f73eb7f1-7a2f-413c-88cd-f2b6ca05e394/image.png)

To ensure precise cessation of axis movement after issuing the **Home** command, the appropriate **input links** must be configured prior to pressing the **Home** button, as depicted in the above explanation. This configuration ensures that the machine accurately detects the home position for each axis.

For example:

- The input **HomePin,X** is assigned to detect the **X-axis** home position. This means that when the X-axis sensor aligns in front of its designated home sensor, the system identifies it as the home position.
- Similarly, other axes such as **Y** , C , **Z** require their respective input links, such as **HomePin,Y** or **HomePin,C**, to be properly set based on the machine's axes and sensor alignment.
    
    This structured setup allows the machine to halt each axis movement accurately when it reaches its home position, ensuring safe and reliable operation during homing procedures.
    

<aside>
❗

**Please note that , Typically, XY Cutter CNC machines do not use home sensors due to the length of the axis.**

</aside>

---

### L**imit pin**

In CNC machines, **limit pins** serve as an essential safety feature to prevent the machine axes from exceeding their physical boundaries. These pins are linked to **hard limit switches**, which are mechanical or sensor-based devices that stop the machine when triggered.

While **Radonix controllers** also provide **soft limits** within the software settings, hard limits add an extra layer of protection and ensure the machine operates safely in unexpected situations.

**Key Points about Limit Pins:**

1. **Hard Limits:**
    - Hard limits rely on physical **limit switches** installed on the machine.
    - When an axis reaches the limit switch, the corresponding **input link** (e.g., **G-LimitPin,X**, **G-LimitPin,Y**, or **G-LimitPin,Z**) is triggered.
    - The machine automatically stops to avoid damage to mechanical components.

1. **Soft Limits:**
    - Soft limits are defined within the **Radonix settings**.
    - The operator sets the allowable movement range for each axis through software, ensuring the axis does not move beyond these defined boundaries.
    - These limits are monitored digitally and act as a preventive measure before reaching the physical hard limits.
2. **Dual Safety Mechanism:**
    - Combining **hard limit pins** with **soft limits** ensures maximum protection:
        - **Soft Limits** act as the first line of defense to stop movements within software-defined boundaries.
        - **Hard Limits** serve as a final physical safeguard to prevent any accidental overrun of the machine axes.

**Configuration of Hard Limit Pins:**

To set up hard limits in Radonix controllers:

1. Navigate to **System > InPorts** in the Radonix software.
2. Assign the input links for the respective limit switches:
    - **G-LimitPin,X** for the X-axis hard limit.
    - **G-LimitPin,Y** for the Y-axis hard limit.
    - **G-LimitPin,Z** for the Z-axis hard limit.
3. Ensure the **Enabled** parameter is set to **True**.

**limitPin,X**          

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/3e85ecfd-fe2a-45b6-afd7-b504480166a6/image.png)

**LimitPin,-X   ///   LimitPin,Y   ///   LimitPin,-Y  ///   LimitPin,Z    ///  LimitPin,-Z**

---

# Inputs and Outputs that necessary in Install process

Certain **inputs and outputs** in XY Cutter include Flame cutters and Plasma CNC machine are fundamental for its proper operation and safety. These links are vital for controlling key components like torch,  motors, sensors, and safety mechanisms. Additionally, there are other links that, while not critical, enhance functionality and provide added convenience. These will be explained further in this section.

## Functions

Functions are commands that can be invoked and executed in various ways (digital input definition, software screen button definition, M-Code definition, remote or keyboard button definition, etc.). Each function includes a number of arguments that determine the type of operation it performs. The functions of the Cutter interface include the following:

Cut-C: Used to enable or disable the C-CutPin output, which includes the following arguments: 

➢ C-Cut,0: Invoking this function deactivates the C-CutPin output. 

➢ C-Cut,1: Invoking this function activates the C-CutPin output.

 ➢ C-Cut,2: Each invocation of this function toggles the state of the C-CutPin output from off to on or from on to off (operates as a toggle).,

**ManualCut-C**: In Cutter interfaces, operators have the capability to run the loaded design once in Demo mode without activating the cutting output and at high speed (the speed for this mode can be adjusted from the Setting→System→ToolPath→TraverseVelocity section). This allows operators to ensure the correct execution of the design and that the entire cutting path is properly aligned with the raw material. To activate this mode, we use the C-ManualCut function, which includes the following arguments:

➢C-ManualCut,0: Invoking this function deactivates the Demo mode. 

➢ C-ManualCut,1: Invoking this function activates the Demo mode. 

➢ C-ManualCut,2: Each invocation of this function toggles the Demo mode between active and inactive (functions as a toggle).

## Inputs

**C-Cutsensorpin** : If this input is defined, the device will pause after the output C-CutPin is activated and wait for this input to be activated. Immediately after this input is activated, the device will continue the cutting process. The presence of the word 'sensor' in the name of this input does not necessarily mean that there is a sensor to detect the completion of the Cut process. This input could be a push button that the operator can press to activate it.”

**C-PreCutSensorPin** : If this input is defined, the device will pause after the output C-CutPinPre is activated and will wait for this input to be activated. Immediately after this input is activated, the device will resume the cutting process. As explained above, the presence of the word 'sensor' in the name of this input does not necessarily imply the existence of a sensor for detecting the completion of the PreCut process. This input could be a push button that the operator can press to activate it.

**FreeSensorPin-C**: If the Z-axis of the device is equipped with a standard DC or AC motor and its movement upwards or downwards is controlled by two separate relays, this input can be used in the presence of a microswitch or a sensor that limits upward and downward movement .As a result, for the microswitch or sensor that limits upward movement, use the input linked with C-ZFreeSensorPin,1, and for downward movement, use the input linked with C-ZFreeSensorPin,-1

## **Outputs**

**C-PreCutPin:** This is the initial or pre-cut output that activates after the device reaches the cutting point. If the input C-PreCutSensorPin is defined in the inputs section, the output remains active until this input is activated and deactivates upon activation of C-PreCutSensorPin. If C-PreCutSensorPin is not defined, this output deactivates after a duration determined by the PreCutTime parameter and proceeds to the next stage. In this case, the operator can bypass the pre-cut timing by invoking the C-Cut function (pressing the Cut button) and enter the cutting stage directly.

**C-CutPin** : This is the second stage output or cutting output, which becomes active after the completion of the first stage, but the device does not move. After this output is activated, if the input C-CutSensorPin is defined in the inputs section, the device will start moving and perform the cutting operation upon activation of this input. If C-CutSensorPin is not defined, the device will start moving and perform the cutting operation after a duration determined by the C-CutTime parameter. In this case, the operator can bypass the cutting timing by invoking the Run function (pressing the Play or Start button) and begin moving along the cutting path.

**C-PreCutPin+CutPin**: This output is active when either the CutPin-C or PreCutPin-C outputs are active. If both outputs are deactivated, this output also deactivates.

**PreCutPin+CutPin+PostCutPin-C**: This output is active when any of the outputs CutPin-C, C-PreCutPin, or C-PostCutPin are active. If all three outputs are deactivated, this output also deactivates. 

**C-PostCutPin**: This output is activated immediately after the cutting process is completed and the CutPin-C output is deactivated. The device stops at that point. After a duration determined by the C-PostCutTime parameter, the device starts moving again and proceeds to the next point to begin cutting.

**FreePin-C**: For devices where the Z-axis is equipped with a standard DC or AC motor and its movement upwards or downwards is controlled by two separate relays, two separate outputs can be defined to control this axis via software or a remote. For this purpose, the output linked with C-ZFreePin,1 is defined for the upward-moving relay, and the output linked with C-ZFreePin,-1 is defined for the downward-moving relay.

## Parameters

**AutoCut**: If the inputs CutSensorPin-C and PreCutSensorPin-C are not defined, and if the value of this parameter is set to True, once the device reaches the starting point of the cut for each piece, the output C-PreCutPin is activated. After the lapse of the PreCutTime, the output C-CutPin automatically becomes active, and after the lapse of CutTime, the device automatically starts cutting. However, if this parameter is set to False, after reaching the starting point of the cut for each piece, the output C-PreCutPin is activated and waits until the operator activates the output C-CutPin. After the C-CutPin is activated, the operator must press the start button for the device to begin cutting the piece.

**CutTime**: If the input CutSensorPin-C is not defined and the parameter TrueAutoCut= is set to true, the device will pause for the duration specified in this parameter after the output C-CutPin is activated, and then it will begin cutting the piece. The unit of this parameter is determined by the TimeUnit parameter.4

**CutVelocity**: If the operator needs to manually cut a part of the piece without a cutting plan, this can be achieved by activating the output C-CutPin and using the manual movement keys (JOG). Under these circumstances, the movement speed of the device is determined by this parameter, which is measured in millimeters per second (mm/s).

**JogDisplaceReferenceEnable**: If the value of this parameter is set to True, in addition to the Continuous mode for manual movement of the device, a third mode is added which is determined by Step. In this mode, the reference position or zero of the workpiece will shift by the same amount as the device's movement. If the value of this parameter is set to False, this mode will no longer be displayed. It is worth mentioning that the Type parameter of this button, unlike other interfaces, is of the Button type and not a Toggle.

**JogMode**: In interfaces where JogDisplaceReference mode exists, to ensure that the manual movement mode, or JogMode, is saved and does not revert to the default setting (Continuous mode) in subsequent software executions, a parameter has been included in the settings to store this mode. Therefore, this parameter does not require special configuration.

**PostCutTime:** This parameter determines the duration of the device's pause after the completion of a cut and the deactivation of the C-CutPin output before moving to the starting point of the next piece to be cut. The unit of this parameter is specified by the TimeUnit parameter.

**PreCutTime**: If the input CutSensorPinPre-C is not defined and the parameter TrueAutoCut= is set to true, the device will pause for the duration specified in this parameter after the C-PreCutPin output is activated, and then it will activate the C-CutPin output. The unit of this parameter is specified by the TimeUnit parameter.

**SheetAlignBaseAxis**: This parameter identifies the base axis for calculations related to Sheet Align. More detailed information about this parameter will be provided in the Sheet Align section.

**TimeUnit**: This parameter specifies the unit for time-related parameters. 'ms' stands for milliseconds, and 's' stands for seconds.

## Sheet Align

When placing the workpiece on the cutting table of the machine, there may be conditions that prevent aligning the piece with the motion axes (the workpiece may be placed askew or, in technical terms, not squared).

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/12b0833a-f0d5-4577-a49f-1eafce16f130/image.png)

In these circumstances, it is necessary for the loaded design to rotate around the zero point according to how much the workpiece is skewed relative to the cutting table, so that the design aligns with the workpiece. To calculate the amount of rotation needed for the design, two points on the workpiece must be introduced to the software as shown below, allowing the software to compute the angle of rotation.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/e40d2ed7-f2de-45ab-91dd-a2cedcab2977/image.png)

For this task, after loading the desired design, the cutting nozzle tip should be brought to a point tangent to the edge of the sheet. At the first point, press the P1 button, and at the second point, press the P2 button to introduce these two points to the software. By doing this, a blue line is drawn between these two points, which is exactly tangent to the edge of the workpiece.

[Sheet Aligne.mp4](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/d76b5cb6-b289-4646-9a45-7a2923207034/Sheet_Aligne.mp4)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/759bfc7a-eedb-4175-9a49-122b00702bd2/image.png)

After that, by pressing Sheet Align, the design becomes tangent to the blue line and is completely positioned within the workpiece.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/eab2ee0e-0923-43b9-9409-669806a0495c/image.png)

It should be noted that the greater the distance between the two points P1 and P2, the more accurately this process will be performed. Now, we will have one of the following two scenarios:

**SheetAlignBaseAxis=X**: In this scenario, the points are selected along the X-axis, and the loaded design will align with the line connecting the two points P1 and P2 (as illustrated below):

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/d02385d4-6c55-4135-9ffa-1b03fbedfb24/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/c4b29824-fbf4-4289-bbe6-2ef81c17da6e/image.png)

**SheetAlignBaseAxis=Y**: In this scenario, the points are selected along the Y-axis, and the loaded design will align with the line connecting the two points P1 and P2 (as illustrated below):

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/fadc9def-931a-4705-8080-110759844cb3/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/4177ed46-fbd5-441a-ae86-3373288aed13/image.png)

# **Calibration**

calibration refers to the process of aligning the motion value of an axis with one of the standard units or with a specific value. Common units in industrial devices are usually millimeters, centimeters, meters, inches, feet, degrees, etc., which are available for use based on the need. Therefore, the concept of calibration for the millimeter unit can be expressed as the alignment of the motion value of the desired axis with the millimeter unit. That is, in the case of measuring with measuring tools, the numerical value of the motion of the axis should be consistent with the measured value in millimeters.

In Radonix controller, each axis has the ability to calibrate separately, and even the axes can be calibrated in different units. The variable representing the calibration factor in this controller is the Step variable, which to access it, you need to open the Radonix software and after opening the Setting window, go to the System branch and then the Axis{n} sub-branch ({n} represents the number between 1 to 6, which specifies the axis number.)

This part can fell in categories stepper and servo motors so due to in this categorizing there are different strategies 

## **Servo motors**

At fırst step of calibration  , Electronic Gear Box must be set :

An **Electronic Gear Box** is an integral component in modern servo systems, especially in applications that involve servo motors, like those used in automation and robotics. This technology essentially functions as a virtual gearbox that adjusts the speed and torque of a motor electronically, rather than mechanically. By manipulating the frequency and amplitude of the motor’s input signals, an electronic gearbox can change the output characteristics of the motor to suit specific tasks without needing physical gear changes.

Next step is essential for this subject is : Encoder Resolution

**Encoder Resolution** is a fundamental specification of servo motors, indicating the number of pulses an encoder emits for each complete revolution of the motor's shaft. This specification, expressed in pulses per revolution (PPR), is crucial for defining the precision with which the motor's position, speed, and acceleration can be controlled.

For instance, the Delta servo motor's B2 model features an encoder resolution of 160,000 pulses per revolution. This means that for every full turn of the motor shaft, the encoder generates 160,000 distinct signals. In contrast, the A2 model from the same brand boasts a much higher resolution of 1,280,000 pulses per revolution. This higher resolution allows for even finer control and more precise adjustments, which is essential in applications requiring meticulous positioning and detailed motion control.

High-resolution encoders are particularly beneficial in fields like robotics, CNC machinery, and automated assembly lines, where exact movements are paramount. The greater the encoder resolution, the smaller the movement that can be detected and controlled, enhancing the system’s accuracy and the quality of the output. This capability is crucial for optimizing the performance of high-precision tasks, ensuring that each component operates within tight tolerances and adheres to strict quality standards.

Understanding and setting the encoder resolution appropriately is a critical first step in the calibration of automated systems. It ensures that the machine operates smoothly and that each part produced meets precise specifications, thereby reducing errors and increasing overall efficiency in manufacturing processes. This detailed control over motor movements is what makes modern automated systems capable of performing complex tasks with high reliability and accuracy.

**General Guide to Setting the Electronic Gear Ratio (E.G.) in Servo Drives**

**Overview**

Configuring the Electronic Gear Ratio (E.G.) for servo drives is crucial for optimizing their performance in applications requiring precise motion control. This guide provides a generic approach to setting E.G. in servo drives, using the Delta B2 servo drive as a specific example to illustrate the process.

**Requirements**

- Servo drive with an integrated encoder
- Controller capable of generating pulse signals (e.g., a CNC controller)
- Technical specifications for both servo drive and controller

**Step-by-Step Configuration**

**Step 1: Understand Encoder Resolution**

- **Objective:** Recognize the encoder resolution, which is the number of pulses needed for one complete rotation of the servo motor's shaft.
- **General Info:** Encoder resolution is specified in pulses per revolution (PPR). It determines the precision with which the servo drive can control the motor position.

**Step 2: Calculate Motor Speed in Rounds Per Second**

- **Objective:** Convert the desired motor speed from RPM (revolutions per minute) to RPS (revolutions per second) to match the controller's output frequency.
- **Procedure:**
    - Formula: RPS=RPM/60
    - This calculation adjusts the time base from minutes to seconds, facilitating synchronization with pulse output.

**Step 3: Determine Required Pulses Per Second**

- **Objective:** Calculate the total pulses per second required based on the RPS and encoder resolution.
- **Procedure:**
    - **Objective:** Calculate the total pulses per second required based on the RPS and encoder resolution.
    - **Procedure:**
        - Multiply the RPS by the encoder resolution to get the required pulses per second.
        - Example Formula: Pulses per Second=RPS × Encoder Resolution
            
            **Pulses per Second=RPS ×Encoder Resolution**
            

**Step 4: Set the Electronic Gear Ratio (E.G.)**

- **Objective:** Adjust the electronic gearing to enable the controller's output to meet the servo motor's pulse requirements.
- **Procedure:**
    
    ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/c5bebdf7-6317-4d2a-9a27-e271e89105ee/image.png)
    
    E.G.=Required Pulses /  Controller’s Pulse Capability 
    
    - Adjust the controller's settings to match the calculated E.G. ratio.

**Example: Delta B2 Servo Drive**

- **Motor Speed:** 3000 RPM
- **Encoder Resolution:** 160,000 PPR
- **Controller's Pulse Capability:** 500,000 pulses per second
- **Calculation:**
    - Convert RPM to RPS: 3000 / 60 = 50
    - Required Pulses: 50×160,000 = 8,000,000
        
        8,000,000 pulses per second=50×160,0008,000,000 \, \text{pulses per second} = 50 \times 160,000
        
    - E.G.: E.G.=16=8,000,000 / 500,000
        
        E.G.=16=8,000,000500,000\text{E.G.} = 16 = \frac{8,000,000}{500,000}
        
    - Set E.G. Ratio: 16:1

**Testing and Validation**

- **Objective:** Ensure that the servo system functions correctly under the new settings.
- **Procedure:**
    - Conduct a test run to check the accuracy and responsiveness of the servo drive.
    - Observe the motion to confirm that it aligns with expected parameters.

**Additional Notes**

- Refer to specific servo drive manuals for detailed specifications and advanced settings.
- Regular maintenance checks and recalibration are recommended to sustain optimal performance.

This comprehensive approach ensures that various types of servo drives can be efficiently integrated and operated in systems requiring high precision, such as in automation and robotics.

now based on this E.G calibration process can be feasible through two ways 

1- Radonix CAM Calibrator and Measurement 

2-Mathematics Calculation 

### **1. Radonix CAM Calibrator and Measurement**

In the calibration method that relies on physical measurements using tools and instruments, the process directly depends on the accuracy of these tools and the inherent mechanical precision of the device being calibrated. This measurement-based method, while not as precise as computational approaches that utilize exact mathematical models and software simulations, is nonetheless popular in many practical applications. It offers a straightforward approach when detailed information about the motor, gearbox, pulley, and gears is unavailable or incomplete.

The fundamental principle of this calibration method involves measuring the actual displacement that occurs for a given number of pulses emitted by the system. By doing so, it allows for direct observation and adjustment based on real-world outcomes, which is particularly valuable in scenarios where theoretical data may not fully capture the dynamics of the mechanical system. The method's reliance on physical measurements means that any error in the measuring tools or mechanical inaccuracies in the system can significantly affect the quality and reliability of the calibration.

Despite its limitations in precision compared to computational methods, this approach is widely adopted because it provides a practical, hands-on way to ensure that machinery and systems are performing within acceptable limits. It is particularly useful in maintenance scenarios or when setting up new equipment in a manufacturing line where detailed specifications of components are not readily available. This method ensures that operators can still achieve effective calibration, maintaining operational efficiency and reducing downtime due to misalignment or other issues arising from improper calibration.

To enhance accuracy and speed in calibration by measurement, Radonix provides a complimentary software tool, CAM-Pro Calibrator. This tool is automatically installed with the main Radonix software suite. It efficiently calculates the step value by measuring the physical displacement of the axis and the required number of pulses for achieving this displacement.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/73cdda73-acaf-41ce-8f60-6b996441c704/image.png)

Since pulse counting in this method is managed by the controller, there is no measurement error associated with pulses. Therefore, the measurement accuracy in this method is directly related to the accuracy of the physical measurement. Additionally, increasing the distance between two measured points results in a higher pulse count, effectively enlarging the denominator of the fraction. With the error remaining constant, the calculated step value becomes more precise. Consequently, calibration based on two widely spaced points will yield more accurate results .

Please note that two Radonix software programs should never be run simultaneously. If they are, one of the programs will not be able to connect online. Therefore, always ensure that all other Radonix software programs are closed before running the desired application.

As explained in the previous section, the CAM-Pro Calibrator software is installed alongside the CAM-Pro software. There are two methods to locate the calibrator software after installation. According to the first method, simply go to the installation location, which by default is on the C drive of Windows. Then navigate to the 'Program Files (x86)' folder, open the Radonix folder, and you will find the Radonix CAM-Pro file where the CAM-Pro Calibrator software can be seen. According to the second method, just use the Search feature from the Start menu (Figure 1, Step 1), search for 'Radonix CAM-Pro Calibrator', and run it

![Untitled.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/5ab811b9-b9b8-432a-8225-9072d501eb6c/Untitled.png)

This program consists of two windows. The first window only appears if there are multiple active interfaces on a computer (Figure 3). Through this window, you can select the desired interface and launch it by pressing the 'Ok' button. If there is only one active interface on the computer, the interface selection window will not open, and the main window will open directly.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/aba06863-0e6c-4b4e-aeac-482ddcc9dc4e/58e902a1-88e2-4099-92c2-4d2c4c8716ea.png)

When you open the CAM-Pro Calibrator software, you will see Figure (4), which components are as follows:

![Untitled.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/65b2eea5-95e6-469c-8dd0-ff0a16e73a07/Untitled.png)

1. **Connection**:
    - ProLan controllers must be set to **LAN mode**.
    - ProUSB controllers must be set to **USB mode**.
2. **Serial**:
    - Displays the controller's serial number.
3. **Activation Code**:
    - Displays the 16-digit code used to activate axes.
4. **Active Axes**:
    - Shows the number of activated axes using the activation code.

---

**Axis Section**

**5.Axis**:

- Allows selecting the desired axis for calibration.

**6.Direction**:

- Select the appropriate movement direction for standard axes:
    - **Negative**: Movement towards the negative direction.
    - **Positive**: Movement towards the positive direction.

**7.Step**:

- Sets the step size for calibration or output pulses. After calibration, the step is automatically recorded in the settings.

---

**Continuous Jog Section**

**8.Negative Jog**:

- Enables manual movement in the negative axis direction.

**9.Jog Mode**:

- Allows selecting the jog movement type:
    - **Continuous**: Smooth, uninterrupted movement.
    - **Incremental**: Moves in defined steps.

**10.Positive Jog**:

- Enables manual movement in the positive axis direction.

**11.Length**:

- Defines the incremental movement distance when the **Incremental** mode is active.

**Velocity Section**

**12.Velocity**:

- Used to set the speed for manual movements.
- The positive and negative buttons next to the **Velocity** option increase or decrease the speed of manual movements.

---

**Calibration Section**

**13.Start**:

- Button to initiate the calibration process.

**14.Location 1**:

- Used to set the initial position for calibration.
- This position must be relative to a fixed point on the measured axis.

**15.Location 2**:

- Used to set the final position for calibration.
- This position must also be relative to a fixed point on the measured axis.

**16.Calibrate**:

- Button to complete the calibration process and calculate the calibration factor.

**17.Exit**:

- Button to exit the calibration program.

---

**To calibrate an axis, follow these steps:**

 First, select the desired axis from the Axis section for calibration. Then, by selecting a low speed and moving the axis, ensure the direction of movement is correct. If the movement direction is incorrect, choose the appropriate direction using the Direction section. Next, move the axis to one of the two ends of its travel range. Since the starting direction in this method is not important, it does not matter which end of the axis is chosen as the starting point. Once the axis is in the correct position, measure a point on the axis relative to a fixed point on the machine using an appropriate measuring tool, record this at Location 1, and press the Start button. Note that unit selection is entirely optional, so if calibration with a specific unit is required, all measurements should be based on that unit. For example, the device can be calibrated in units of inches, meters, centimeters, millimeters, or even micrometers.

Move the axis to the opposite end. If measurements at greater distances are possible and the measuring tool is sufficiently accurate, measurements over longer distances will yield more precise results. After moving the axis to the second point, measure this point similar to the first relative to the fixed point on the machine, record this at Location 2, and then press the Calibrate button. Using these measurements, the calibration step or factor is calculated and automatically registered in the designated interface. The calibration process can be repeated as many times as needed for each axis.

Please note that if the activation code has not been entered, an error message will be displayed when opening the CAM-Pro Calibrator software.

### **Calibration Validation Method in Radonix CAM-Pro Software**

To ensure the accuracy of calibration settings applied to the CNC machine, you can follow the steps below:

1. **Select Axis and Manual Movement:**
    
    Start by selecting the axis you want to validate (e.g., the **X-axis**). Use the **Continuous Jog** mode to manually move the machine to a specific position.
    
2. **Mark the Position:**
    
    At the current position of the machine, mark a reference point on the machine's body or the work surface. This mark will be used as a reference for measurement.
    
3. **Switch Jogging Mode:**
    
    Change the jogging mode from **Continuous** to **Incremental**. This mode allows the axis to move by precise, predefined values.
    
4. **Enter Desired Distance:**
    
    In the **L(mm)** box (located above the Jog buttons), input the desired distance for the axis to move. For example, enter **1000 mm**.
    
5. **Execute the Movement:**
    
    Press the Jog button corresponding to the desired direction (positive or negative) for the axis. The machine should move exactly the specified distance (e.g., 1000 mm).
    
6. **Measure the Position:**
    
    After the machine stops, measure the actual distance traveled by the axis using a precise measuring tool, such as a ruler or caliper.
    
7. **Verify Calibration:**
    
    The measured distance should match the value entered in the software (e.g., 1000 mm). If there is a discrepancy, the calibration settings may need to be reviewed and adjusted.
    

Inports are divers some of them for Safety, Home sensors , specific sensors related to applications

Inports (when the sensors )are triggered ,the controller sets that position as the zero or origin point for each axis of the machine. Additionally, the corresponding LEDs for their input pins turn on.

---

### 2. Mathematics Calculation

**Computational Method**
To align the axis movement with the desired unit, a calibration coefficient called "Step" is used. To access this variable, first open the software and then navigate to the Setting window, proceed to the System branch, and the sub-branch Axis{n} (where {n} represents a number between 1 and 6, indicating the axis number). The Step variable is located within these sub-branches, and each axis has its own specific Step variable.

If the unit of axis movement is in millimeters, the unit of this variable will be millimeters per pulse. If the movement unit is centimeters, inches, or any other unit, the Step variable will also be expressed in that unit per pulse. Essentially, this represents the amount of movement of the desired axis per one pulse transmitted to that axis's motor driver. Therefore, to calculate this variable, one must understand the relationship between the motor's movement amount per input pulse to the driver and the conversion ratios of gearboxes, pulleys, and any other type of motion transmission. For a better understanding of these calculations, consider the following examples:

> **Example 1:**
Consider a linear axis of a CNC machine where the measurement unit is in millimeters, and it is equipped with Panasonic A5 motors that have a 10:1 gearbox ratio. This motor is connected via a pinion with an effective diameter of 66 millimeters to a rack. Now, calculate the Step value for the specified axis.
> 

**Please note** that each piece of information plays a crucial role in these calculations and can be used to compute the step size of the axis for calibration purposes. For example, knowing the type of motor driver and its specifications determines the relationship between the input pulse to the driver and the resulting movement of the motor shaft.

In Panasonic A5 motors, at a rate of 500,000 pulses per second, the motor reaches a speed of 3000 rpm. In the first step, we calculate the motor's rotational speed per second. Here, the figure 3000 represents the number of motor revolutions per minute, which we convert to seconds by dividing by 60, the number equivalent to one minute. The result is 50, meaning the motor makes 50 rotations per second. Therefore, the equation can be written as: Motor rotational speed per second = 3000 rpm / 60 s = 50 r/s. In the second step, we need to calculate the amount of axis movement per one rotation of the motor.

In fact, in this example, the distance traveled will be equal to the circumference of a circle, and the circumference of a circle is calculated as the diameter of the circle multiplied by π (pi) Or approximately 3.1415 meters. As mentioned in Example 1, a pinion with a diameter of 66 millimeters and a 10:1 gearbox are used in the mechanics, so we will have The amount of axis movement per one revolution of the motor is calculated as (1/10) * 66(mm) * 3.1415 = 20.7339 mm  The result obtained is the amount of axis movement per one rotation.

The final step is to write the ultimate equation and find the unknown value, which in this case is the Step variable. As observed, all calculations are based on 500,000 pulses sent by the controller and a motor speed of 3000 rpm. Therefore, to calculate the movement or distance traveled per 1 pulse, the result obtained needs to be divided by 500,000. However, as stated earlier, this motor makes 50 revolutions per second. Thus, it is important to note that while the amount of movement was calculated per 1 revolution in the second step, the motor completes 50 revolutions per second. Therefore, the number obtained in the second step must be multiplied by 50 to find the total distance traveled per second by the motor. Now, we will rewrite the overall equation once more.

Step(mm/pulse) = 50(r/s)∗20.7339(mm) / 500000(pulse/s) = 0.00207339 (pulse/mm)

$$
Step(mm/pulse) = 50(r/s)∗20.7339(mm) / 500000(pulse/s) = 0.00207339 (pulse/mm)
$$

From this equation, the Step value is calculated. This value means that the motor moves 0.0207339 millimeters per 1 pulse received.

Please note that the computational method used in Example 1 is intended for the calibration of linear axes.

Step(unit/pulse) = The value of the axis movement per one rotation of the motor *  the number of motor rotations per second / Number of pulses sent by the controller per second

> **Example 2:** Consider a rotary axis of a CNC machine where the measurement unit is in degrees. It is equipped with Panasonic A5 motors, which have a 25:1 gearbox connected to a 12-tooth pulley. This pulley is then linked via a belt to a 44-tooth pulley. Now, calculate the Step value for the specified axis.
> 

Motor rotational speed per second = 3000 rpm / 60 s = 50 r/s.

In the final step, we must multiply the effective values, such as the gearbox ratio, the pulley ratio, and the motor's rotational speed per second, by 360. As we observed, all calculations are based on 500,000 pulses sent by the controller and a motor speed of 3000 rpm. Therefore, to calculate the movement per 1 pulse, we must divide the obtained value by 500,000. This simple estimation will yield the Step value.

Step= 50(r/s)∗(1/25)∗(12/44)∗360 / 500000(pulse/s) = 0.000392727272

From this equation, the Step value is calculated.

The general equation for calibrating rotary axes is as follows:
Step(unit/pulse) = Rotation amount per second in the motor * effective value * 360 *    / Number of pulses sent by the controller per second 

> **Please note** that whether calculating linear axes or rotary axes, the more significant digits we use, the more precise the calculation results will be.
> 

> **Please note** Pulse divisions in stepper motors directly impact these calculations. For simplicity, one can first calculate the motor rotation for a specific pulse value and then incorporate the result into the equations above.
> 

> **Please Note** In drives where the number of pulses required to reach the maximum motor speed exceeds the number of pulses produced by the controller, one can achieve the maximum motor speed by increasing the electronic drive ratio to a specific extent. For example, if a drive requires 4 million pulses per second to reach the maximum motor speed, and considering that Radonix produces 500,000 pulses per second, an electronic drive ratio of 8 should be considered to achieve the maximum rotational speed of the motor.
> 

---

After opening any DXF file, the DXF Reader window automatically opens and displays the components contained in the file.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/900ad95d-0676-416a-b590-a79bfd3b8030/image.png)

The toolbar below this window includes the following items:

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/2864648c-8cf7-4af0-a0d6-fa42e8abb60b/image.png)

The Zoom Fit button, which when clicked, displays the opened design fully within the DXF Reader window.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/07c0620d-8455-4b99-86e5-ab785392c725/image.png)

The Zoom Out button, which when clicked, reduces the scale of the opened design by one level. Additionally, you can perform the Zoom Out action by holding the mouse pointer over the design and scrolling the Mouse Wheel upwards.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/cb5652be-7e8a-4485-9ea6-262a4f33fea6/image.png)

By clicking on this option, the opened design enlarges by one level. Additionally, you can perform the Zoom In action by holding the mouse pointer over the design and scrolling the Mouse Wheel downwards.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/dee8ef4b-b2f0-4dde-b66c-7eaca072e0c9/image.png)

This option is used to determine the position of the Reference point or zero of the workpiece in the opened design, which includes the following items:

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/290da9b1-8274-49b3-a24a-78802ee5d2c0/image.png)

This option considers the bottom right corner of the shape, or in other words, the endpoint in the positive direction of the X-axis and the endpoint in the negative direction of the Y-axis, as the zero point.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/6757d87e-fb28-45fe-b20b-0781bdfc5613/image.png)

This option considers the top right corner of the shape, or in other words, the endpoint in the positive direction of the X-axis and the endpoint in the positive direction of the Y-axis, as the zero point.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/d01fdc0d-aa7b-4e2a-b8c8-9dcf1b434e3b/image.png)

This option considers the top left corner of the shape, or in other words, the endpoint in the negative direction of the X-axis and the endpoint in the positive direction of the Y-axis, as the zero point.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/ff16885d-ad04-4988-8521-f9c3b1408f0e/image.png)

This option considers the top left corner of the shape, or in other words, the endpoint in the negative direction of the X-axis and the endpoint in the positive direction of the Y-axis, as the zero point.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/6ad8cd26-7a59-4263-9bc3-8be08b504cb6/image.png)

This option considers the starting point of the first piece in the opened design as the zero point.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/16783673-20b9-4f52-931c-8a32ffa1c710/image.png)

This option is used for applying rotation (Rotate) or mirroring (Flip) to the design, which includes the following items:

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/5800de9f-0f38-4e42-b67e-637f34e25c77/image.png)

90-degree rotation clockwise.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/378187aa-c8d8-442e-8a85-0f1f7addf0fd/image.png)

90-degree rotation counterclockwise.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/55ef6b67-a5e9-4733-b1b2-8900126aa70d/image.png)

Mirror across the X-axis

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/186e0259-98aa-4f91-9af0-5c4d744dafa6/image.png)

Mirror across the Y-axis.

In any design file, by default, parts are cut in the same sequence as they are drawn in the design software, and the start and end points of each cut are chosen based on the direction of the line drawn in the design software. However, in the DXF Reader section, the order and direction of the part cuts can be changed as desired. When you open a DXF file, by default, all parts are active for execution and the cutting direction is specified.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/c5cf64d7-5dde-45ab-b111-4a60d3e50818/image.png)

By clicking on the 'Arrange Objects' option, all parts are deactivated. By left-clicking on any part, it becomes activated for cutting, and by clicking again, it is deactivated. Additionally, by right-clicking on parts, you can reverse the cutting direction. If we have selected a number of parts for which the order of execution is important .for selecting the rest of the parts for which the order of execution does not matter from  Select objects 

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/8984df19-1b8b-4d10-be9e-64db3d127bb0/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/e4cc23a8-f22a-40ce-b664-a235ea3fa0bd/image.png)

The 'Default Arrange' option is for executing the design in the default order set by the design software. The 'Optimize' option selects the order of part cuts in such a way that minimizes the execution time of the file (the order of cuts is arranged such that after finishing the cut of one part, the closest starting point to the endpoint of the previous part is chosen).

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/a97b1307-1ff5-4a96-928b-e8c7136c90e9/image.png)

Clicking on this option selects only the parts that are in Polyline form for cutting, and deactivates the parts that do not have this feature.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/6f3b26de-e040-4d54-ba93-324aebc4ce48/image.png)

The pink lines displayed in the figure are non-cutting or Traverse lines, which indicate the path of the machine's movement when transitioning between two different pieces. Clicking on this option allows you to activate or deactivate the display of these lines.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/0bd73a6b-7bb2-4530-b469-7d264cae136a/image.png)

This section determines the cutting speed of the parts, and the unit is millimeters per second. Note that this speed only specifies the machine's movement speed during cutting and does not affect the machine's travel speed between two different pieces within a design.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/74c3674b-0900-4148-a540-8e2e480d5c74/image.png)

After completing modifications on the loaded file, by clicking on this option, while preserving the original file, you can save your changes before executing the file to avoid the need for re-editing the design in future runs. It should be noted that the file is saved with a .CNC extension as a G-Code file, and it cannot be edited in subsequent runs.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/fcc70d8b-ba3b-40c8-9745-670c99fc149c/image.png)

By clicking on this option, without saving changes, the DXF Reader window will close, and the design will be loaded and ready for execution.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/8881640a-a2ce-435d-b9be-fda56aa6138c/image.png)

By clicking on this option, the DXF Reader window will close without loading the design.

# **Tips on setting up different cutting machines:**

CNC Oxy-Fuel Cutting Machine: In oxy-fuel cutting machines with an automatic ignition system, separate solenoid valves on the gas output, pre-heated air, and oxygen for cutting, the outputs are defined as follows: ➢ C-PreCutPin: Automatic ignition 

➢ C-PreCutPin+CutPin: Solenoid valve for gas output and solenoid valve for pre-heated air output 

➢ C-CutPin: Solenoid valve for oxygen cutting or jet 

The PreCutTime parameter can be used to control the duration of molten pool formation. 

The CutTime parameter can be used to control the duration it takes to pierce the workpiece.

 Considering that the outputs of the control board supply a maximum current of 200 milliamps to the consumer and drawing more current than this amount can damage the output, even if using a 24-volt solenoid valve, avoid directly connecting the solenoid valve to the control board and always use a relay.

In machines where the distance from the solenoid valves to the cutting nozzle is significant and the length of the intermediary hose is long, to prevent damage to the end part of the cut, be sure to use the PostCutTime parameter. This ensures that the machine pauses until the gas in the hoses is fully discharged, preventing damage to the workpiece.

A significant part of the cutting quality in CNC oxy-fuel cutting machines depends on the operator's skill in adjusting the flame and the distance of the cutting nozzle to the workpiece.
