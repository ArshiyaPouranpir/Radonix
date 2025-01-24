# **Introduction**

The XYZ Router - TC interface serves as a user interface between the operator and advanced software for a three-axis CNC machine, featuring capabilities such as automatic tool change, support for various types of linear and rotary parking systems, and digital output control during G-code execution via M-Code. Complementary features like the ability to connect an XBOX controller and keyboard as remote controllers, automatic park position adjustment, and the definition of up to 6 reference points for work start positions make machine operation easy and precise for operators. All inputs and outputs are pre-configured by default, so no additional programming is required. The interface can also be customized visually to fit the industrial needs and branding of manufacturing companies.

One of the key advantages of Radonix software and interfaces is the ability to install, set up, and display G-code in 3D while performing various settings such as defining digital inputs and outputs, adjusting speed, acceleration, and other related parameters. These settings can even be tested and simulated in G-code mode without requiring hardware. This feature allows users to gain an initial understanding of Radonix controllers’ performance and functionality, significantly simplifying the setup and configuration process.

<aside>
💡

**This interface is called XYZ Router +TC**

For starting primary installation there are some steps to go throw it and has a successful installing

</aside>

## **Interface workspace**

1- Study about different part of interface which is named and indicated in photo it means that you should get familiar with all elements like Buttons , screen , bars , volume , values , … anything on interface you have accesses

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/dbdc8197-acae-4486-b963-470383b49d98/image.png

# Get Start

## Workspace Descriptions

Here's a detailed description of each section and button on this CNC controller interface

---

### **Top Status Bar**

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/2f12e0d3-037a-41d0-8fc1-7850de5aef2e/image.png

- **Online** (Yellow Light): Indicates the machine's connection status. Yellow may mean a standby mode or that it's not fully online.(FAQ)
- **X Axis, Y Axis, ZAxis** (Green Lights): These lights show the operational status of each axis. Green typically means these axes are active or ready.(FAQ)
- **Alarm, Emergency** (Brown Lights): Indicators for critical safety statuses. When activated, they may change color (e.g., red) to signal an alarm, emergency stop.(FAQ)

---

### **Position and Speed Readouts (Right Panel)**

- **Absolute Position** (Top Right Box):

**Absolute**: Displays the coordinates of the axes in reference to the
home point.(FAQ)

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/8684a6e6-9bff-45e6-8091-7fb4ee5bdd81/image.png

- **Relative Position** (Besides Absolute Position):

**Relative :** Shows the coordinates of the axes relative to the
reference point.

- **Velocity** (Below Relative Position): Shows the current operational speed in mm/s, useful for monitoring real-time cutting or movement speeds.(FAQ)

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/61a85014-05b9-479e-9ffb-3710f82addc9/image.png

---

### **Position Controls (Mid Right Panel)**

- **Home** (Target Icon): Moves the machine to its home or origin position.

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/98ad66cd-a99f-41b3-bf2c-dc536d130283/image.png

- **X0 , Y0** **, Z0** (Crosshair Icons): These buttons take spindle to the X , Y , Z coordinates to zero or move the tool to the zero point in each axis.(FAQ)

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/1e5a144f-9c89-48e0-85e0-8f8a89482620/image.png

- You have two options for saving reference points. The first option is to manually move the tool by jogging, and when you reach the desired point, press the corresponding button to save that position for the axis. The second option is to directly enter the precise position value in the input box in front of each button.

### **Manual Jogging Controls**:

- **Arrows** (X+, X-, Y+, Y-): These buttons manually jog the machine along the X and Y axes, allowing for precise positioning adjustments by moving the tool head incrementally.

You can switch the jog mode by pressing this button according fig 01-05  and it will change to figure 01-06, changing from continuous to incremental movement. This means you can define a value in this section according fig 01-07 which has been indicated in red area , and after pressing the coordinate axis jog, the axis will move by the amount you have entered.

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/db482cae-aebb-4230-943d-909d0acb25f6/image.png

```
  —————————————————————————————————

```

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/a2899a09-3ae6-4d6f-913f-dbf2f3dfd682/image.png

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/99c1a585-6b60-4dfc-ad18-b92fca03545d/image.png

---

---

---

---

---

---

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/f7907150-5699-4d9d-911e-528326b66fb9/image.png

---

### **Feed Rate and Tool Parameters (Lower Right Panel)**

- **V (mm/s)** and Step**(mm)**: Input fields for setting feed rates and movement limits along each axis. "V" controls the velocity (or speed) in mm/s, and "L" could define the step size for each manual jog.

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/ff26cb42-900d-450a-b68f-44c446b33764/image.png

- **Scroll** (Vertical Slider on Bottom Right ):According to figure 01-08 which is demarcated with red area or Allows for real-time adjustment of the feed rate or speed as a percentage. This control can quickly change the speed without directly altering program values.

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/cb4a5c30-b24b-4449-9472-fdb95f29d4a4/image.png

---

### **Main Program Controls**

- **Settings (Gear Icon)**: Opens the configuration menu, where detailed settings for the CNC machine can be adjusted.

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/39410150-1ffb-4b43-bb4d-d39e1eed380a/image.png

- The Exit icon allows you to close the program
- The Minus icon lets you minimize it.

---

Interface specification :

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/8f7ba062-a675-49c0-a8d9-6769a47da8a1/image.png

This section of the interface displays the current status and features of the system. It also updates to show alarms and processes every second. For a detailed report, double-click on this section.

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/763c7cce-77be-4258-be28-1700fa8ad1a4/image.png

---

### **Main Program Controls (Bottom Center)**

- **Open File** (Folder Icon): Opens a file dialog for loading a CAM (Computer-Aided Manufacturing) file, typically a G-code or DXF program.

---

---

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/bd296a18-ae51-4e1c-8991-28ee89e25aff/image.png

This section is dedicated to controlling G-Code execution:

- **RUN**: This button starts the G-Code process.
- **Pause**: This button halts the toolpath.
- **Reset**: This button resets the toolpath.

---

### **Spindle Button and Scroll Rotation Control**

### **Spindle Button and Scroll Rotation Control**

- **Spindle Button:**
    
    The spindle button allows the operator to manually control the spindle, enabling it to be turned **on** or **off** as needed. This provides flexibility for tasks that require direct manual control of the spindle’s operation.
    
- **Spindle Rotation Control:**
    
    The spindle rotation speed can be **adjusted** using the scroll control. By rotating the scroll, the operator can precisely set the spindle’s rotational speed, ensuring optimal performance for specific cutting or machining tasks.
    

---

### **Tool Management in TC-Enabled Interfaces**

In CNC interfaces with the **Tool Change (TC)** option, such as the **XYZ Router + TC**, the following features are provided:

1. **Tool Number:**
    
    The interface allows the operator to select and display the desired tool number. This ensures the correct tool is used for the operation.
    
2. **Set Tool:**
    
    The **Set Tool** button issues an order to take the selected tool to the **Tool Height Sensor**. This process automatically measures the tool height, ensuring accurate calibration and alignment of the tool with the workpiece.
    

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/6888a4b0-4165-4bc1-88e4-bbe13ae95bee/image.png

### **Display and Zoom Controls (Center of Main Display)**

- **Grid Display** (Black Area with Grid): Shows the work area and toolpath visualization. The grid assists in visualizing the relative position of the tool and workpiece.

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/b308b93d-64d3-4ce4-94a5-aa6accdd75a4/image.png

- **Zoom and Pan Controls**:
    - **+ and - Buttons**: Zoom in and out on the display.
    - **Circle Icon**: switching between different mode.
    - **Box Icons** (Bottom Right of Grid): control additional viewing or display .

---

## **Special Functions**

- **Support for Various Router Types**:
    - Up to **6 simultaneous axes** for applications like wood, stone, milling, mold making, and dental work.
- **Rotation Tool Center Point (RTCP)**:
- RTCP support ensures accurate rotary toolpath calculations.
- **Multi-Spindle Head Support**:
    - Ideal for machines requiring multiple spindles.
- **Automatic Tool-Changing Devices**:
    - Supports **linear**, **rotary**, and **jack-type** tool changers.
- **Tool Offset Sensors**:
    - Automatic **Z-axis tool offset** sensing and referencing for precision.
- **3D Tool Path Display**:
    - Visualization of tool paths, including support for **rotary axes**.
- **Loading Depth Restriction**:
    - Floor depth restrictions for controlled operations.

---

# Initial Setup: Configuring Settings and Wiring for Peripheral Integration

In this section, it is essential to comprehend the configuration of the inputs and outputs to effectively manage their operation.

## **Applying Changes in Radonix**

When making any changes in the **Radonix Cam Pro software**, it is essential to follow a specific process to ensure that all updates are properly applied and functional throughout the system. This process ensures that settings are saved and initialized correctly.

**Steps for Applying Changes**

1. **Make the Changes:**
    - Navigate to the appropriate section (e.g., Inputs, Outputs, System Settings).
    - Modify the desired parameters or configurations.
2. **Press the Set Button:**
    - After making changes, click the **Set** button to confirm and apply them throughout the software.
3. **Close the Program:**
    - Completely close the Radonix Cam Pro software after saving changes.
4. **Reopen the Program:**
    - Restart the software to initialize the updated settings and ensure they are loaded properly.

# Inputs and Outputs Structure

**Inputs**:

- **Purpose**: Inputs receive signals from various sensors or external controls (like limit switches, emergency stops, or user interfaces).
- **Types**: Common input types include digital (e.g., ON/OFF signals) and analog (e.g., varying voltage levels).
- **Configuration**: Inputs are configured to trigger specific responses in the CNC system. For instance, an emergency stop input might trigger all operations to halt immediately.

**Outputs**:

- **Purpose**: Outputs actuate machinery components, like motors, valves, or lights, based on the commands from the CNC system’s processing unit.
- **Types**: Outputs can be relay-based (for high power applications) or transistor-based (NPN or PNP for direct control with less power).
- **Protection Features**: As in Radonix models, outputs often have protections such as short-circuit prevention, overload protection, and error indication to ensure safe operation.

---

**In summary**, the **CTRL + SHIFT + ALT + Delete** shortcut is a powerful diagnostic tool for real-time inspection of your CNC system’s internal state. By utilizing this feature and reviewing additional information in **Appendix 4**, you can more easily troubleshoot and optimize your Radonix CNC machine’s performance.

## Inputs and Outputs in Radonix Cam Pro

**Location:**

Inputs and outputs in the Radonix Cam Pro software are typically managed through a dedicated section of the software interface is located in Setting / System /  Inports or Outports.

These settings allow users to configure and customize the behavior of the machine's physical and virtual components to meet specific operational needs.

**Accessing Inputs and Outputs**

1. Navigate to the **Settings** menu.
2. Select **System** to open the configuration options.
3. Choose either **Inports** or **Outports** to access the respective settings.

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/e32a71f8-d18c-4a92-a884-55bde9315d08/image.png

**Expanding Input/Output Sections**

- Beside each part (**Inports** or **Outports**), you will find a **plus (+) button**.
- Clicking this button will expand the section, revealing the configuration options for individual inputs or outputs.

### How you can monitor all inputs and outputs together

**Overview**

In Radonix CAM-Pro software, you can quickly view the status of the controller’s internal variables, axes, inputs, and outputs using a special diagnostic shortcut. This is particularly helpful for troubleshooting issues related to sensors, axes movement, or output signals.

> Shortcut: CTRL + SHIFT + ALT + Delete
> 

Press **CTRL + SHIFT + ALT + Delete** to open an on-screen display that shows:

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/31dbd53d-9a62-48b6-b2e8-d3a24a71c46d/image.png

1. **Internal Variables:**
    - Real-time values of key parameters such as feed rates, acceleration values, and any custom variables used in your CNC programs.
2. **Axes Status:**
    - Current positions of the X, Y, Z (and any additional) axes.
    - Movement states (e.g., jogging, homing, paused).
    - Activation status (green lights) indicating whether each axis is online and responsive.
3. **Inputs and Outputs:**
    - A list of digital inputs (limit switches, sensors, emergency stops) and their live state (ON/OFF).
    - A list of digital outputs (relays, spindle on/off signal, pneumatic valves) and whether they are currently active or inactive.

**Usage Scenarios**

- *Wiring Diagnostics:**Confirm that a limit switch or sensor correctly toggles from OFF to ON when physically triggered.
- *Axis Verification:**Check whether the software is correctly commanding each axis to move, and whether the axis is acknowledging motion.
- *Signal Confirmation:**Verify if the controller is sending the correct signal to external hardware (e.g., spindles, vacuum pumps, coolant systems).

**Tips & Notes**

- The **CTRL + SHIFT + ALT + Delete** shortcut is unique to the Radonix CAM-Pro software and is **not** the same as the standard Windows **CTRL + ALT + Delete** function.
- If nothing appears on your screen after using the shortcut:
    - Ensure that Radonix CAM-Pro is running and the controller is powered on.
    - Verify that you are using the correct key combination in the proper sequence.
- If you encounter persistent issues or see unexpected values in the diagnostic view, consult your system administrator or contact Radonix technical support.

---

---

# Inports

In this section, we will examine the configuration of the Inputs.

Essentially, when the Inports branch is opened, these settings will appear.

**Setting Up Inputs: General Overview**

Configuring inputs in our CNC system is an essential step to ensure smooth operation, precise control, and safety. Inputs can be categorized into two main types based on their configuration and purpose: **Hardware-Based Inputs** and **Software-Based Inputs.** This flexibility allows the system to adapt to a wide range of applications and machine requirements.

---

## **1. Hardware-Based Inputs**

Hardware inputs involve physical devices connected to the controller, enabling direct interaction with the machine's environment. These inputs are crucial for safety, machine control, and real-time feedback.

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/b6bf2353-d2c8-46e5-b817-7852a26c6ed7/image.png

The digital inputs of Radonix controllers are named as I.[n], where n is a number greater than zero and represents the input number. These inputs are isolated by optical couplers and have low noise tolerance due to their low impedance.

The digital inputs on Radonix controllers have the capability to switch between NPN and PNP modes depending on the output of the device or sensor. The mode changeover switch must be set to PNP position for devices with PNP output and NPN position for devices with NPN output.

In various branches of industrial automation, there are equivalent terms for PNP and NPN. Some
examples of these terms include:
NPN = Sink = Low Active
PNP = Source = High Active

### **Switching Between PNP and NPN Modes in Radonix Systems**

The ability to switch between **PNP** (positive logic) and **NPN** (negative logic) modes in Radonix controllers depends on the specific **board model** being used. This flexibility allows the system to be compatible with different wiring and sensor configurations.

- **PC Pro LAN:**
    - A **small DIP switch** is present on the board.
    - This switch allows users to toggle between **PNP** and **NPN** modes.
    - **How to Use:**
        - Locate the DIP switch on the board.
        - Toggle the switch to the desired mode (PNP or NPN).
        - Ensure the board is powered off before making changes to prevent damage.
            
            !https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/5234e53a-523b-434b-be9f-d99db25f2795/image.png
            
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
        
        !https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/ba60d093-16bc-4c0e-aa31-cc53ea55edea/image.png
        

### **Examples of Hardware Inputs:**

- **Limit Switches:** Define physical boundaries for axis movement.
- **Home Sensors:** Establish the reference (Home) position for the machine most of them are **Proximity**
- **Emergency Stop Buttons:** Ensure immediate halting of operations in emergencies.
- **Other Proximity Sensors:** Detect objects or tools in the machine's workspace.
- **Push Buttons and Selector Switches:** Trigger specific machine functions or modes.
- **Scanners:** Measure or detect specific properties, often used in specialized processes such as Glass **or gold CNC operations**.

### **Configuration Process**

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

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/4bc60a0b-b42f-4c30-9f75-4b33a0192ea7/image.png

As illustrated in the figure, each input is divided into three sub-branches, as detailed below:

1. **Enable**: This sub-branch can be set to two values: True or False.
2. **Link**: Specifies the duty or task that needs to be performed or checked. This includes any device that can serve as an input, such as sensors, buttons, and switches.
3. **NC**: Determines whether the specific input is Normally Open (NO) or Normally Closed (NC).

### **Examples of Software Inputs**

- **Virtual Limit Switches:**
    - Use software parameters to define axis movement boundaries based on the machine's table size.
- **Logical Triggers:** Define conditional triggers for specific operations (e.g., When the axis reaches the limit switch ).
- **Simulated Inputs:** Use for testing or scenarios where physical components are unavailable.

### **Configuration Process**

1. **Access Configuration Interface:**
    - Open the controller's software settings to manage inputs.
2. **Define Parameters:**
    
    ```
     As an example to set  limit Switch :
    
    ```
    
- setting —→ System —→ In ports —→ Enabled= True
    
    ```
                                                                              Linked = LimitPin,X
    
                                                                               NC= True
    
    ```
    
- Configure additional logical conditions for interlocks or simulations.
1. **Validate Settings:**
    - Test the software by CAM Pro TEST input configurations to ensure proper functionality and safety.

### **Setting Up Inputs**

**Simple and Intuitive Configuration**

In Radonix system, configuring inputs or Outputs  is designed to be as user-friendly as possible, without requiring any microprogramming or advanced technical knowledge. All you need to do is navigate to the **Inputs** section of the controller interface, open the settings drawer, and select the item you need to configure. The same process applies to other sections, such as **Outputs** or any other functional areas.

---

**Step-by-Step Configuration Process**

1. **Access the Desired Section:**
    - Go to the section you want to configure, such as **Inputs** or **Outputs**, depending on the functionality you are setting up.
2. **Open the Settings Drawer:**
    - Within the selected section, locate the specific input branch or subsection.
    - Click or expand the settings drawer to reveal the available options.
3. **Select the Required Item:**
    - Choose the input type or functionality you want to configure (e.g., limit switch, home sensor, emergency stop, or custom inputs).
    - Define the specific role for the input, such as `LimitPin, X` or `HomePin`.
4. **Set Parameters Easily:**
    - Adjust the necessary parameters, such as polarity (Normally Open or Normally Closed), response delays, or logical behavior, directly from the interface.
5. **Save and Test:**
    - Save your settings and validate them through the controller interface to ensure everything is functioning as intended.
    - **In the end in order to finalizing you have to close program to save everything**

---

### **Key Features of the Configuration System**

- **No Microprogramming Needed:** The intuitive design ensures you can make all necessary configurations without writing code or using low-level programming tools.
- **Centralized Interface:** Everything is accessible through a single, organized interface, making it easy to navigate between different sections.
- **Flexibility:** Configure both hardware and software inputs effortlessly, adapting the system to meet your specific operational needs.
- **Error-Free Setup:** The graphical interface minimizes the chances of errors, ensuring a seamless configuration process.

**Essentially, once the interface is installed, it comes with a default setup, and everyone can change the order of the input ports. For instance, we include necessary Inports which are effective and suitable for the initial launch  .**

The first recommended step for providing protection against any errors or mistakes is to define the Emergency link. This can be connected to a button that either stops the motors or turns off the digital outports.

---

---

# Outputs

In this section, we will examine the configuration of the Outputs.

**Setting Up Inputs: General Overview**

In Radonix systems, **Outports** are critical components that manage the output signals controlling various peripherals, such as relays, actuators, alarms, and other devices. Outputs can be categorized into two main types based on their configuration and purpose: **Hardware-Based Inputs** and **Software-Based outputs.**
This flexibility allows the system to adapt to a wide range of applications and machine requirements.

## **1. Hardware-Based Outputs**

Hardware outputs involve physical signals sent from the controller to external devices, enabling direct control of the machine’s environment. These outputs are critical for operational safety, machine actuation, and real-time command execution, ensuring efficient workflow and coordination within the CNC system.

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/0272e6ad-833a-4b06-9733-bc681e5375dd/image.png

The digital outputs of Radonix controllers are named O.[n], where n is a numerical identifier greater than zero and represents the output number .

Radonix controllers incorporate robust protection mechanisms for **Outports** to ensure durability, safety, and reliability. These mechanisms vary between different models, specifically the **PC-Pro** and **PC-Smart** boards, each with distinct protection features and failure handling processes.

### **Output Behavior in PC-Pro LAN Models**

- The **PC-Pro LAN** model outputs are fixed in **NPN mode**.
- **How It Works:**
    - When an output is **ON**, it provides **0 volts** by pulling the signal to ground.
    - When an output is **OFF**, it is in a high-impedance state, effectively disconnecting the circuit.
- **Wiring Consideration:**
    - Connected devices must be compatible with NPN logic, where the load receives voltage from a positive source and is activated when the output pulls the circuit to ground.
    
    !https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/3a3aca22-7fd6-4428-b66c-19b01731118a/image.png
    

### **Output Behavior in PC-Smart Models**

- The **PC-Smart** model offers a flexible configuration where outputs can operate in **PNP mode** or **NPN mode**, depending on the connection of the **COM Pin**.
- **How It Works:**
    - The voltage provided by the outputs depends on what is connected to the **COM Pin**:
        - **COM Pin Connected to 24V:** Outputs will provide **24 volts** when activated.
        - **COM Pin Connected to Ground:** Outputs will provide **0 volts** when activated (NPN mode).
- **Flexibility:**
    - This design allows PC-Smart models to adapt to different wiring requirements and device logic preferences.
    
    !https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/455205eb-8c3c-4cd8-815d-b73826fbc9e6/image.png
    

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/50ea19ad-9754-4df1-ab4a-9e36161d058d/image.png

### **Configuration Process for Outputs:**

1. **Connection:**
    - Physically connect the hardware component (e.g., relay, electric valve , Barke , alarm) to the designated output pin on the controller.
    - Ensure proper wiring based on the required logic (PNP or NPN) and voltage compatibility.
2. **Output Definition:**
    - Use the controller software to define the role of the output (e.g., `SpindleCWpin`, `Coolant`,`SpindelCoverpin` or a custom output for specific functions).
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

!https://prod-files-secure.s3.us-west-2.amazonaws.com/26629e82-13c9-4084-96dd-228aca52449f/b512b422-ab71-4d34-b86c-b63400cf26da/image.png

As illustrated in the figure, each output is divided into three sub-branches, as detailed below:

1. **Enable**: This sub-branch can be set to two values: True or False.
2. **Link**: Specifies the duty or task that needs to be performed or checked. This includes any device that can serve as an output, such as actuators, lights, and alarms.
3. **NC**: Determines whether the specific output is Normally Open (NO) or Normally Closed (NC).

### **Examples of Software Outputs**

- **Virtual Relays:**
    - Use software parameters to define activation boundaries for devices based on operational needs.
- **Logical Triggers:** Define conditional triggers for activating specific outputs (e.g., alarms or Relay for specific function ).
- **Simulated Outputs:** Employ these for testing or in scenarios where physical components are not available.

### **Configuration Process**

1. **Access the Configuration Interface:**
    - Navigate to the controller's software settings to manage outputs.
2. **Define Parameters:**
    - To configure an output like an order to forward the VFD, enter parameters.
    - setting —→ System —→ Outports —→ Enabled= True
        
        ```
                                                                                   Linked = SpindleCWPin
        
                                                                                   NC= True
        
        ```
        
3. **Validate Settings:**
    - Test the configured software outputs to ensure they function correctly and safely, verifying their effectiveness in real-world applications.

### **Setting Up Inputs**

**Simple and Intuitive Configuration**

In Radonix system, configuring inputs or Outputs  is designed to be as user-friendly as possible, without requiring any microprogramming or advanced technical knowledge. All you need to do is navigate to the **Inputs** section of the controller interface, open the settings drawer, and select the item you need to configure. The same process applies to other sections, such as **Outputs** or any other functional areas.

**Step-by-Step Configuration Process**

1. **Access the Desired Section:**
    - Go to the section you want to configure, such as **Inputs** or **Outputs**, depending on the functionality you are setting up.
2. **Open the Settings Drawer:**
    - Within the selected section, locate the specific input branch or subsection.
    - Click or expand the settings drawer to reveal the available options.
3. **Select the Required Item:**
    - Choose the input type or functionality you want to configure (e.g., limit switch, home sensor, emergency stop, or custom inputs).
    - Define the specific role for the input, such as `SpindleCWPin`
4. **Set Parameters Easily:**
    - Adjust the necessary parameters, such as polarity (Normally Open or Normally Closed), response delays, or logical behavior, directly from the interface.
5. **Save and Test:**
    - Save your settings and validate them through the controller interface to ensure everything is functioning as intended.
    - **In the end in order to finalizing you have to close program to save everything**

---

---

---
