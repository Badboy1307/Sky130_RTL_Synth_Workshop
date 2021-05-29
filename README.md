

# Sky130 RTL Design and Synthesis Workshop

VSD Sky130 RTL was a five day workshop where I have learnt about the open source tools used in the VLSI Industry, timing liberties, hierarchical and flat synthesis concepts, optimization in both sequencial logic and combinational logic circuitry codes, GLS Blocking and non blocking statements and finally I have learnt about the optimization techniques used during synthesis of both logic and combinational logic circuitry codes . I will be briefly explaining about these topics daywise and I'll be cataloging my sail of these 5 days workshop.


![image](https://user-images.githubusercontent.com/60011091/119861437-04d26000-bf35-11eb-9515-85b05a1788d5.png)  ![image](https://user-images.githubusercontent.com/60011091/119867192-4108bf00-bf3b-11eb-9e46-4544afc0c9fa.png)


# DAY1- Verilog RTL Simulation, Synthesis and Design 

## RTL Simulation  

![image](https://user-images.githubusercontent.com/60011091/119868845-318a7580-bf3d-11eb-816c-7fef5d3e4eb0.png) 



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

Synthesizer is a tool to convert RTL Code to netlist. Yosys is the synthesizer used in the workshop. Constraints are the guidance offered to the synthesizers.

![download (1)](https://user-images.githubusercontent.com/60011091/119988279-8bde1180-bfe3-11eb-9cba-d385700603a2.png)

![Untitled Workspace (1)](https://user-images.githubusercontent.com/60011091/120014223-6eb73c00-bfff-11eb-8ba8-080a895ecea8.png)



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


The output loads in digital circuits are mostly capacitive loads.
When charging or discharging of capacitance is faster, the cells have lesser delays for this to happen we need transistor capable of sourcing more current.

Faster cells has a tradeoff in power and area even though it has lesser delays for a given design.

Wider transistors has low delays but greater power and area for a given design specifications. On the other hand narrower transistors has high delays but lesser powe and area from the same design specifications.

## Yosys introduction lab 

![Capture5](https://user-images.githubusercontent.com/60011091/120017907-0fa7f600-c004-11eb-897b-6bbe22ec4d35.JPG)

![Capture6](https://user-images.githubusercontent.com/60011091/120019417-0d469b80-c006-11eb-9e22-26c943b2fb59.JPG)

![Capture7](https://user-images.githubusercontent.com/60011091/120019809-8219d580-c006-11eb-8998-f876fe49907e.JPG)

![Capture8](https://user-images.githubusercontent.com/60011091/120020022-ce651580-c006-11eb-9591-7c2ba233c6b9.JPG)

![Capture9](https://user-images.githubusercontent.com/60011091/120020131-f3598880-c006-11eb-9742-f6c6c835e7bd.JPG)

![Capture10](https://user-images.githubusercontent.com/60011091/120021034-2c462d00-c008-11eb-88be-e0dccef19b6f.JPG)

![Capture11](https://user-images.githubusercontent.com/60011091/120021160-526bcd00-c008-11eb-880c-af66a429ae95.JPG)


![Capture12](https://user-images.githubusercontent.com/60011091/120021523-cc03bb00-c008-11eb-97f0-eac9dbb78b88.JPG)


sky130_fd_sc_hd__o21ai_1 in netlist visualization has 3 inputs and 1 output as it has 2 input OR  gate into first input of 2input NAND gate. sky130_fd_sc_hd is a high density digital standard cell contributed Skywater foundry.


## Day-2 Timing libs , Hierarchy vs flat synthesis and efficient flop styles

# .lib file lab 
![Capture13](https://user-images.githubusercontent.com/60011091/120023408-5c42ff80-c00b-11eb-9695-e9d3daf567db.JPG)

![Capture14](https://user-images.githubusercontent.com/60011091/120023428-62d17700-c00b-11eb-9f33-de5ab2ef58a3.JPG)

![Capture15](https://user-images.githubusercontent.com/60011091/120023495-7aa8fb00-c00b-11eb-960e-ab05706f992b.JPG)

sky130_fd_sc_hd__tt_025c_1v80.lib --> has 025c as temperature parameter, 1v80 as voltage parameter and tt which is a typical process parameter.

![Capture18](https://user-images.githubusercontent.com/60011091/120025121-d83e4700-c00d-11eb-8e61-636ed6b56637.JPG)


# Hierarchy vs flat Synthesis lab 

Hierarchy Synthesis

![Capture16](https://user-images.githubusercontent.com/60011091/120024686-2ef75100-c00d-11eb-98bc-2082e617716f.JPG)

![Capture17](https://user-images.githubusercontent.com/60011091/120024695-30c11480-c00d-11eb-9893-60a9777b6f6d.JPG)

![Capture19](https://user-images.githubusercontent.com/60011091/120025454-526ecb80-c00e-11eb-9062-72e7be2122c8.JPG)

![Capture20](https://user-images.githubusercontent.com/60011091/120025621-9792fd80-c00e-11eb-9f28-ec621cad920f.JPG)

![Capture21](https://user-images.githubusercontent.com/60011091/120025794-d6c14e80-c00e-11eb-88f9-8d5bc2e02420.JPG)

![Capture22](https://user-images.githubusercontent.com/60011091/120025891-f48eb380-c00e-11eb-9464-2859ee503b48.JPG)


![Capture23](https://user-images.githubusercontent.com/60011091/120026094-30c21400-c00f-11eb-9cba-28fe3515c2cd.JPG)


![Capture24](https://user-images.githubusercontent.com/60011091/120026330-8ac2d980-c00f-11eb-9822-41a2a49d049e.JPG)

![Capture26](https://user-images.githubusercontent.com/60011091/120027056-8945e100-c010-11eb-90be-0430255b4d53.JPG)

Flat Synthesis 

![Capture27](https://user-images.githubusercontent.com/60011091/120027495-0e30fa80-c011-11eb-9812-65ac466afb91.JPG)

![Capture28](https://user-images.githubusercontent.com/60011091/120027691-4fc1a580-c011-11eb-8bb7-1f36dd655bbf.JPG)

Submodules

![Capture29](https://user-images.githubusercontent.com/60011091/120028253-1178b600-c012-11eb-8b6f-70770b408aed.JPG)

![Capture30](https://user-images.githubusercontent.com/60011091/120028309-25241c80-c012-11eb-905a-b8b2d2a14be0.JPG)

![Capture31](https://user-images.githubusercontent.com/60011091/120028566-76341080-c012-11eb-9ccf-0748ec1895ba.JPG)

![Capture32](https://user-images.githubusercontent.com/60011091/120028549-703e2f80-c012-11eb-9e4f-d255969134d5.JPG)



# Why Flops and Flops Designs 

![image](https://user-images.githubusercontent.com/60011091/120029004-1db14300-c013-11eb-9a98-e2900ac64a09.png)

The above image shows the comparison Asynchronous reset, Asynchronous set , Synchronous reset and Synchronous reset.


# Lab for Flop styles

Using Simulator and Waveform viewer

Asynchronous reset

![Capture34](https://user-images.githubusercontent.com/60011091/120029558-e727f800-c013-11eb-9a8e-2e69f1e86435.JPG)

![Capture35](https://user-images.githubusercontent.com/60011091/120029806-35d59200-c014-11eb-9056-f23897ae7033.JPG)

Asynchronous set

![Capture36](https://user-images.githubusercontent.com/60011091/120030107-a7154500-c014-11eb-9c81-65c59975dda8.JPG)

![Capture37](https://user-images.githubusercontent.com/60011091/120030248-da57d400-c014-11eb-8e0d-5fa73442be08.JPG)


Synchronous reset

![Capture38](https://user-images.githubusercontent.com/60011091/120030551-3e7a9800-c015-11eb-8018-7beaaf449fbe.JPG)

![Capture39](https://user-images.githubusercontent.com/60011091/120030736-7681db00-c015-11eb-9e40-1346fcf12382.JPG)
![Capture39](https://user-images.githubusercontent.com/60011091/120031140-07f14d00-c016-11eb-972e-d4290d765d93.JPG)

Using Synthesizer for Asynchronous reset


![Capture40](https://user-images.githubusercontent.com/60011091/120031276-396a1880-c016-11eb-8f0e-2e77df970772.JPG)

![Capture42](https://user-images.githubusercontent.com/60011091/120031373-5999d780-c016-11eb-9ee7-169938a1988e.JPG)


![Capture41](https://user-images.githubusercontent.com/60011091/120031223-26efdf00-c016-11eb-969c-f911f6101c66.JPG)

![Capture42](https://user-images.githubusercontent.com/60011091/120031791-e349a500-c016-11eb-93af-460837e1db61.JPG)

![Capture43](https://user-images.githubusercontent.com/60011091/120031797-e5abff00-c016-11eb-8a98-ce60607a1bd5.JPG)

![Capture44](https://user-images.githubusercontent.com/60011091/120031970-27d54080-c017-11eb-96b3-b5f9f030a33d.JPG)


![Capture45](https://user-images.githubusercontent.com/60011091/120032098-52bf9480-c017-11eb-8104-3f7e8c9ed2ea.JPG)


#Interesting Optimizations

![Capture46](https://user-images.githubusercontent.com/60011091/120056558-b323f580-c05a-11eb-8dfc-070a2d07193a.JPG)


![Capture47](https://user-images.githubusercontent.com/60011091/120056581-d2bb1e00-c05a-11eb-80c6-a98560b97fd6.JPG)


![Capture48](https://user-images.githubusercontent.com/60011091/120056613-0433e980-c05b-11eb-954d-49ea21be1ea4.JPG)


Synthesis 

![Capture49](https://user-images.githubusercontent.com/60011091/120056712-b370c080-c05b-11eb-9510-8b7c29d53e4c.JPG)


![Capture50](https://user-images.githubusercontent.com/60011091/120056780-12363a00-c05c-11eb-84a5-dcd8631ab7f2.JPG)


![Capture51](https://user-images.githubusercontent.com/60011091/120056796-2aa65480-c05c-11eb-9459-5df27bb118a8.JPG)



![Capture52](https://user-images.githubusercontent.com/60011091/120056840-5e817a00-c05c-11eb-83b7-ae71f8596c17.JPG)


Design 

![Capture53](https://user-images.githubusercontent.com/60011091/120056868-8c66be80-c05c-11eb-9c52-944f50cd174d.JPG)


## Day-3 Combinational and Sequential Optimizations

# Combinational  Optimizations
Logics are squeezed to obtain the most optimized design in terms of Area, Power savings

# Methods for Combinational  Optimizations
1) Constant propagation (direct optimization)
2) Boolean Logic Optimization (K map, Quine McKluskey)









 


