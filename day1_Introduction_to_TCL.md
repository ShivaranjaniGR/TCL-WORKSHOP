

# DAY 1
## 🧠 Introduction to TCL

TCL (Tool Command Language) is a powerful scripting language widely used in VLSI design automation and EDA tools. This 10-day workshop, conducted by VLSI System Design (VSD), provides hands-on training in TCL scripting for automating design workflows. It is tailored for students and professionals aiming to strengthen their VLSI scripting skills. Each session builds practical knowledge through guided labs and real-world examples.

---
## 🔧 Virtual Environment Setup Using VDI

On the first day of the TCL workshop, I completed the setup of the virtual lab environment by following the instructions provided in the *StepsToOpenTCL_Labs.pdf*. This included downloading the required VDI file, configuring a virtual machine using Oracle VirtualBox, and successfully launching the Ubuntu-based lab system. With the virtual environment properly configured, I am now prepared to begin the TCL lab sessions in a controlled and consistent workspace.

---
##  🔍 Learning Objectives

By completing this task, we will:

- Gain proficiency in **TCL scripting** for VLSI automation
- Learn how to parse external inputs like Excel and integrate file I/O in TCL
- Understand **pre-layout timing analysis** in digital designs
- Build a reusable and scalable **automation framework**

---
## About the Project
### 🎯 Project Objective

To develop a **TCL-based User Interface (UI)** system that:
- 📥 Takes an **Excel sheet as input**
- 📤 Produces a **design datasheet (pre-layout timing report)** as output

This flow is automated through a TCL script (`SynthTime.tcl`), also referred to as the **TCL box**.



### 📦 Input – Excel Sheet

The Excel sheet acts as a **design descriptor**, containing key information such as:

- ✅ **Design Name**  
- ✅ **Top-Level Module Name**  
- ✅ **Netlist Directory** – where the RTL (e.g., Verilog) source files are stored  
- ✅ **Output Directory Path** – where the TCL scripts will dump outputs
 <img width="413" height="257" alt="image" src="https://github.com/user-attachments/assets/254fafc5-3af8-49c9-ad6b-b4f4661b0e2d" />


This behavioral input is essentially a blueprint for a digital processor or RTL design.



### ⚙️ The TCL Box (`SynthTime.tcl`)

At the heart of the project is a script engine called the **TCL box**, implemented in the file `VSDSynth.tcl`.  
It is responsible for:
- 🔍 Parsing the Excel sheet  
- 📂 Accessing the required files and directories  
- 📊 Generating pre-layout timing analysis reports

We focus on building this box step-by-step, covering all script internals and data handling workflows.



### 📄 Output – Pre-Layout Timing Datasheet

The final output of this system is a **pre-layout timing report** — a datasheet that provides early insights into the performance and characteristics of the RTL design, before physical synthesis.

---

## ⚙️ Tasks and tools needed
- Create command (for eg. SynthTime) and pass .csv from UNIX shell to TCL script

- Convert all inputs to format[1] & SDC format, and pass to synthesis tool ‘Yosys’
  - Create variables  
  - Check if directories and files mentioned in .csv, exists or not  
  - Read “Constraints File” for above .csv and convert to SDC format  
  - Read all files in “Netlist Directory”  
  - Create main synthesis script in format[1]  
  - Pass this script to Yosys


- Convert format[1] & SDC to format[2] and pass to timing tool ‘Opentimer’

- Generate output report

---



