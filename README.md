

# Sky130 RTL Design and Synthesis Workshop

VSD Sky130 RTL was a five day workshop where I have learnt about the open source tools used in the VLSI Industry, timing liberties, hierarchical and flat synthesis concepts, optimization in both sequencial logic and combinational logic circuitry codes, GLS Blocking and non blocking statements and finally I have learnt about the optimization techniques used during synthesis of both logic and combinational logic circuitry codes . I will be briefly explaining about these topics daywise and I'll be cataloging my sail of these 5 days workshop.


![image](https://user-images.githubusercontent.com/60011091/119861437-04d26000-bf35-11eb-9515-85b05a1788d5.png)  ![image](https://user-images.githubusercontent.com/60011091/119867192-4108bf00-bf3b-11eb-9e46-4544afc0c9fa.png)


# DAY1- Verilog RTL Simulation, Synthesis and Design 

## RTL Simulation  

![image](https://user-images.githubusercontent.com/60011091/119868845-318a7580-bf3d-11eb-816c-7fef5d3e4eb0.png) 

![Untitled Workspace (1)](https://user-images.githubusercontent.com/60011091/120014223-6eb73c00-bfff-11eb-8ba8-080a895ecea8.png)

![image](https://user-images.githubusercontent.com/60011091/119868918-46670900-bf3d-11eb-8873-ab8074c8f015.png)


Simulator is a tool for examining the correctness of your design. RTL design is the implementation of a given specification.The intent of specification needs to be verified by simulating the design. iverilog was used for simulation of a given design. Simulator looks for changes in the input signal and so if there is no change in the input signal of a design the output will reflect the same value given in the input signal.

Design can be an actual code or set of Verilog code whose functional intention is to meet a required specification and it should be a synthesizable verilog code. Design may have one or more  primary inputs and primary outputs depending on the design specifications.



Testbench is an another verilog file which consists of instantiation of the top level module of a given design and it doesn't necessarily needed to be synthesizable code. But testbench doesn't really have primary inputs or any primary outputs.


![Untitled Workspace](https://user-images.githubusercontent.com/60011091/120012023-948f1180-bffc-11eb-9821-b828b086ce18.png)



The above image shows the flow of iverilog simulator whose inputs consist of design files and testbenches of the design and the value change dump (vcd) file is our output file.

In the very same image we see that the output file of iverilog that is our vcd file is sent as input to gtk wave which is a vcd waveform viewer where we can check the correctness of a particular design logic which can be a simple or a complex circuit or can be a combinational or sequential circuit designs.


## LAB1- Setting up the Lab 

Here I'll be covering how we are going to setup our lab server to simulate, view and synthesis the given specification of a design.

Initially we will be creating a VLSI directory using mkdir VLSI and then we cd into the directory using cd VLSI as shown below

![image](https://user-images.githubusercontent.com/60011091/119877385-98f8f300-bf46-11eb-8ece-f88d6dcbdde4.png)

Here we use ls commmand to list out all the files in that particular directory as shown in the above image. 

Before git cloning any repository in linux platform we can use sudo -i to enter root directory or by directly cloning that particular repository to the present folder and then we need to check whether git package is already installed if not install it using sudo apt-get install git.

Now that the  prerequisites of git cloning are done we need to start cloning vsdflow repository and sky130 RTL Design and Synthesis Workshop for this workshop.

VSDFLOW repository can be cloned by git clone https://github.com/kunalg123/vsdflow.git

![image](https://user-images.githubusercontent.com/60011091/119933860-801e2b00-bfa2-11eb-840f-f84961891174.png)

This image shows the contents of vsdflow directory after cloning its repository.

After the command ./opensource_eda_tool_install.sh is executed, a list of open source tools which get installed are:
a) Yosys is RTL Synthesis tool
b) blifFanout is a high fanout net synthesis tool.
c) graywolf is a tool used specifically for placement phase 
d) qrouter is used as a tool for  detailed routing of the design
e) magic is a tool to extract GDSII layout file as well as carries out DRC and Antenna checks.
f) netgen is a tool for checking Lsyout vs Schematic for a given design
g) OpenTimer & OpenSTA are STA (Static timing analysis) tools

sky130 RTL Design and Synthesis Workshop can be cloned by 
![image](https://user-images.githubusercontent.com/60011091/119934398-5a455600-bfa3-11eb-940b-284ad3037d96.png)


This image displays all the contents of sky130 RTL Design and Synthesis Workshop directory in a detailed fashion.

![image](https://user-images.githubusercontent.com/60011091/119973629-5b8d7780-bfd1-11eb-8b1f-80c757205c5e.png)

![image](https://user-images.githubusercontent.com/60011091/119974182-03a34080-bfd2-11eb-9eb7-d86c0487c58a.png)

These two images displays all the subfolders of  my_lib, lib and verilog files in the sky130 RTL Design and Synthesis Workshop directory


## LAB2- iverilog and gtkwave introduction lab

In this lab iverilog was used as simulator and gtkwave for vcd waveform viewer

![Capture](https://user-images.githubusercontent.com/60011091/119986983-23dafb80-bfe2-11eb-9fe8-dcce9e1e009b.JPG)

![Capture_1](https://user-images.githubusercontent.com/60011091/119987012-2b9aa000-bfe2-11eb-875c-d1b7e16bb6fe.JPG)
![Capture_2](https://user-images.githubusercontent.com/60011091/119987022-2e959080-bfe2-11eb-987b-313208d6b607.JPG)
![Capture_3](https://user-images.githubusercontent.com/60011091/119987033-31908100-bfe2-11eb-97f7-bdfe3a660f1e.JPG)
![Capture_4](https://user-images.githubusercontent.com/60011091/119987040-33f2db00-bfe2-11eb-85b1-ddd24472d0d4.JPG)

These images demonstrates how iverilog was used for simulating design code good_mux .v along with testbench tb_good_mux.v and how we view the vcd format file using gtkwave. The final image shows how the design and testbench files are viewed using gedit command.

## Note: The testbench and the design code can be passed using iverilog command in any order. In the above example we can give iverilog good_mux.v tb_good_mux.v or as  
iverilog tb_good_mux.v good_mux.v

## RTL Synthesizer and Logic synthesis

Synthesizer is a tool to convert RTL Code to netlist. Yosys is the synthesizer used in the workshop. 

![download (1)](https://user-images.githubusercontent.com/60011091/119988279-8bde1180-bfe3-11eb-9cba-d385700603a2.png)


![image](https://user-images.githubusercontent.com/60011091/119988024-47eb0c80-bfe3-11eb-8588-06ecbeaab580.png)

The above image shows the flow of yosys. Yosys takes RTL code and .lib files as input and netlist as output. Netlist is the standard cell representation of the design.

From the above image, we use read_verilog to read the design code, read_liberty to read .lib files and finally write_verilog for generating netlist 

We use the very same iverilog flow to verify the synthesis of the design as we did in iverilog lab section.


During the synthesis of netlist verification, the output should be same as that of what what we did in iverilog lab. For synthesis of netlist we will be using the same testbench as used in iverilog and gtkwave lab.

RTL Design is the behavioral representation of the needed specifications.

In Logic synthesis, RTL code is converted to gate level translation and so the connections are made with the gates and finally it's taken out as netlist.

## .Lib files
These are collection of logic modules which consists of basic gates like and, or, not etc and can have different flavors for the same gate.

## Why do we have diiferent flavors of basic gates?

In the logic path, combinational delay determines the maximum speed of operation of digital logic circuits.

![image](https://user-images.githubusercontent.com/60011091/119996267-2b070700-bfec-11eb-9a6e-53f8e29f236e.png)
![image](https://user-images.githubusercontent.com/60011091/119998864-c0a39600-bfee-11eb-8908-761776245f1c.png)


The above images describes the clock cycle process and how it can be calculated. We need faster cell lib for faster clock speed and setup time. But we need slower cells to avoid hold time issues. Collection of fast cells and slow cells form the .lib.

## Faster Cells versus Slower Cells

![image](https://user-images.githubusercontent.com/60011091/119999359-49bacd00-bfef-11eb-9492-a8f6eedc84f5.png)



























 


