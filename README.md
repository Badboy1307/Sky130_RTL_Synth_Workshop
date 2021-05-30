

# Sky130 RTL Design and Synthesis Workshop

VSD Sky130 RTL Design and Synthesis Workshop was a five day workshop conducted by VSD-IAT. I have learnt about the open source tools used in the VLSI Industry, timing liberties, hierarchical and flat synthesis concepts, optimization in both sequencial logic and combinational logic circuitry codes, GLS Blocking and non blocking statements and finally I have learnt about the optimization techniques used during synthesis of both logic and combinational logic circuitry codes . I will be briefly explaining about these topics daywise and I'll be cataloging my journey in this 5 days workshop.


![image](https://user-images.githubusercontent.com/60011091/119861437-04d26000-bf35-11eb-9515-85b05a1788d5.png)  ![image](https://user-images.githubusercontent.com/60011091/119867192-4108bf00-bf3b-11eb-9e46-4544afc0c9fa.png)

## Day wise Workshop topics 

## Table of Contents 
     

- [Day-1 Verilog RTL Simulation Synthesis and Design](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Day-1-Verilog-RTL-Simulation-Synthesis-and-Design)
  * [RTL Simulation](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#RTL-Simulation) 
  * [Lab for Setting up the Lab](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Lab-for-Setting-up-the-Lab)
  * [iverilog and gtkwave introduction lab](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#iverilog-and-gtkwave-introduction-lab)
  * [RTL Synthesizer and Logic synthesis](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#RTL-Synthesizer-and-Logic-synthesis)
  * [.lib files](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#.lib-files)
  * [Yosys introduction lab](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Yosys-introduction-lab) 
   
    
- [Day-2 Timing libs Hierarchy versus flat synthesis and efficient flop styles](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Day-2-Timing-libs-Hierarchy-versus-flat-synthesis-and-efficient-flop-styles)
  * [.lib file lab](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#.lib-file-lab) 
  * [Hierarchy vs flat Synthesis lab](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Hierarchy-vs-flat-Synthesis-lab) 
  * [Lab for Flop styles](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Lab-for-Flop-styles)
  * [Interesting Optimizations](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Interesting-Optimizations)
    
- [Day-3 Combinational and Sequential Optimizations](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Day-3-Combinational-and-Sequential-Optimizations)
  * [Combinational Optimizations](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Combinational-Optimizations)
  * [Sequential Optimizations](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Sequential-Optimizations)
  * [Lab for Combinational Optimizations](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Lab-for-Combinational-Optimizations)
  * [Lab for Sequential Optimizations](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Lab-for-Sequential-Optimizations)
  * [Lab for Sequential Optimizations for unused inputs](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Lab-for-Sequential-Optimizations-for-unused-inputs)
    
- [Day-4 Gate Level Synthesis Synthesis Simulation mismatch and Blocking Non blocking statements](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#DAY-4-Gate-Level-Synthesis-Synthesis-Simulation-mismatch-and-Blocking-Non-blocking-statements)
  * [GLS](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#GLS)
  * [Synthesis Simulation Mismatches](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Synthesis-Simulation-Mismatches)
  * [Lab for GLS Synthesis Simulation Mismatch](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Lab-for-GLS-Synthesis-Simulation-Mismatch)
  * [Lab for Synthesis Simulation Mismatch for blocking statements](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Lab-for-Synthesis-Simulation-Mismatch-for-blocking-statements)
  
- [Day-5 If Case For Loop and for Generate statements](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Day-5 If-Case-For-Loop-and for-Generate statements)
  * [If statements](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#If-statements) 
  * [Case statements](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Case-statements)
  * [Lab for Incomplete If statements](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Lab-for-Incomplete-If-statements)
  * [Lab for Incomplete case statements](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Lab-for-Incomplete-case-statements)
  * [For loop statements and For generate statements](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#For-loop-statements-and-For-generate-statements)
  * [Lab for  For loop statement and For generate statements](https://github.com/Badboy1307/Sky130_RTL_Synth_Workshop/blob/main/README.md#Lab-for-For-loop-statement-and-For-generate-statements)
     
                 

## Day-1 Verilog RTL Simulation Synthesis and Design 

### RTL Simulation  

![image](https://user-images.githubusercontent.com/60011091/119868845-318a7580-bf3d-11eb-816c-7fef5d3e4eb0.png) 



![image](https://user-images.githubusercontent.com/60011091/119868918-46670900-bf3d-11eb-8873-ab8074c8f015.png)


Simulator is a tool for examining the correctness of your design. RTL design is the implementation of a given specification.The intent of specification needs to be verified by simulating the design. iverilog was used for simulation of a given design. Simulator looks for changes in the input signal and so if there is no change in the input signal of a design the output will reflect the same value given in the input signal.

Design can be an actual code or set of Verilog code whose functional intention is to meet a required specification and it should be a synthesizable verilog code. Design may have one or more  primary inputs and primary outputs depending on the design specifications.



Testbench is an another verilog file which consists of instantiation of the top level module of a given design and it doesn't necessarily needed to be synthesizable code. But testbench doesn't really have primary inputs or any primary outputs.


![Untitled Workspace](https://user-images.githubusercontent.com/60011091/120012023-948f1180-bffc-11eb-9821-b828b086ce18.png)



The above image shows the flow of iverilog simulator whose inputs consist of design files and testbenches of the design and the value change dump (vcd) file is our output file.

In the very same image we see that the output file of iverilog that is our vcd file is sent as input to gtk wave which is a vcd waveform viewer where we can check the correctness of a particular design logic which can be a simple or a complex circuit or can be a combinational or sequential circuit designs.


### Lab for Setting up the Lab 

Here I will be covering how we are going to setup our lab server to simulate, view and synthesis the given specification of a design.

Initially we will be creating a VLSI directory using mkdir VLSI and then we cd into the directory using cd VLSI as shown below


    $ mkdir VLSI
    $ cd VLSI
    $ ls

![image](https://user-images.githubusercontent.com/60011091/119877385-98f8f300-bf46-11eb-8ece-f88d6dcbdde4.png)
                   
     $ mkdir VLSI
     $ cd VLSI
     $ ls

Here we use ls command to list out all the files in that particular directory as shown in the above image. 


Before git cloning any repository in linux platform we can use sudo -i to enter root directory or by directly cloning that particular repository to the present folder and then we need to check whether git package is already installed if not install it using sudo apt-get install git.

Now that the  prerequisites of git cloning are done we need to start cloning vsdflow repository and sky130 RTL Design and Synthesis Workshop for this workshop.

VSDFLOW repository can be cloned by git clone
                               
    $ https://github.com/kunalg123/vsdflow.git
    $ cd vsdflow
    $  ls -ltr

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


      $ https://github.com/kunalg123/sky130RTLDesignAndSynthesisWorkshop.git
      $ cd sky130RTLDesignAndSynthesisWorkshop
      $ ls -ltr 
                                  

![image](https://user-images.githubusercontent.com/60011091/119934398-5a455600-bfa3-11eb-940b-284ad3037d96.png)


This image displays all the contents of sky130 RTL Design and Synthesis Workshop directory in a detailed fashion.

    $ cd my_lib 
    $ ls
    $ cd lib 
    $ ls 
    $ cd verilog_models
    $ ls
  

![image](https://user-images.githubusercontent.com/60011091/119973629-5b8d7780-bfd1-11eb-8b1f-80c757205c5e.png)


                                    

![image](https://user-images.githubusercontent.com/60011091/119974182-03a34080-bfd2-11eb-9eb7-d86c0487c58a.png)


These two images displays all the subfolders of  my_lib, lib and verilog files in the sky130 RTL Design and Synthesis Workshop directory


### iverilog and gtkwave introduction lab

In this lab iverilog was used as simulator and gtkwave for vcd waveform viewer



![Capture](https://user-images.githubusercontent.com/60011091/119986983-23dafb80-bfe2-11eb-9fe8-dcce9e1e009b.JPG) 
        
       $ iverilog good_mux.v tb_good.mux.v
       $ ls
       $ ./a.out
       $ gtkwave tb_good_mux.v

#### Simulation and Waveform Viewer

![Capture_1](https://user-images.githubusercontent.com/60011091/119987012-2b9aa000-bfe2-11eb-875c-d1b7e16bb6fe.JPG)           

![Capture_2](https://user-images.githubusercontent.com/60011091/119987022-2e959080-bfe2-11eb-987b-313208d6b607.JPG)

![Capture_3](https://user-images.githubusercontent.com/60011091/119987033-31908100-bfe2-11eb-97f7-bdfe3a660f1e.JPG)


#### Design 

![Capture_4](https://user-images.githubusercontent.com/60011091/119987040-33f2db00-bfe2-11eb-85b1-ddd24472d0d4.JPG)

These images demonstrates how iverilog was used for simulating design code good_mux .v along with testbench tb_good_mux.v and how we view the vcd format file using gtkwave. The final image shows how the design and testbench files are viewed using gedit command.

#### Note: The testbench and the design code can be passed using iverilog command in any order. In the above example we can give iverilog good_mux.v tb_good_mux.v or as  iverilog tb_good_mux.v good_mux.v


### RTL Synthesizer and Logic synthesis

Synthesizer is a tool to convert RTL Code to netlist. Yosys is the synthesizer used in the workshop. Constraints are the guidance offered to the synthesizers.


![download (1)](https://user-images.githubusercontent.com/60011091/119988279-8bde1180-bfe3-11eb-9cba-d385700603a2.png)


![Untitled Workspace (1)](https://user-images.githubusercontent.com/60011091/120014223-6eb73c00-bfff-11eb-8ba8-080a895ecea8.png)



The above image shows the flow of yosys. Yosys takes RTL code and .lib files as input and netlist as output. Netlist is the standard cell representation of the design.

From the above image, we use read_verilog to read the design code, read_liberty to read .lib files and finally write_verilog for generating netlist 

We use the very same iverilog flow to verify the synthesis of the design as we did in iverilog lab section.


During the synthesis of netlist verification, the output should be same as that of what what we did in iverilog lab. For synthesis of netlist we will be using the same testbench as used in iverilog and gtkwave lab.

RTL Design is the behavioral representation of the needed specifications.

In Logic synthesis, RTL code is converted to gate level translation and so the connections are made with the gates and finally it's taken out as netlist.

### .lib files
These are collection of logic modules which consists of basic gates like and, or, not etc and can have different flavors for the same gate.

#### Why do we have diiferent flavors of basic gates?

In the logic path, combinational delay determines the maximum speed of operation of digital logic circuits.

![image](https://user-images.githubusercontent.com/60011091/119996267-2b070700-bfec-11eb-9a6e-53f8e29f236e.png)


![image](https://user-images.githubusercontent.com/60011091/119998864-c0a39600-bfee-11eb-8908-761776245f1c.png)


The above images describes the clock cycle process and how it can be calculated. We need faster cell lib for faster clock speed and setup time. But we need slower cells to avoid hold time issues. Collection of fast cells and slow cells form the .lib.

##### Faster Cells versus Slower Cells


The output loads in digital circuits are mostly capacitive loads.
When charging or discharging of capacitance is faster, the cells have lesser delays for this to happen we need transistor capable of sourcing more current.

Faster cells has a tradeoff in power and area even though it has lesser delays for a given design.

Wider transistors has low delays but greater power and area for a given design specifications. On the other hand narrower transistors has high delays but lesser powe and area from the same design specifications.

### Yosys introduction lab 

     $ yosys
     yosys> read_liberty -lib  ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
     yosys> read_verilog good_mux.v
     yosys> synth -top good_mux
     yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
     yosys> show 
     

![Capture5](https://user-images.githubusercontent.com/60011091/120017907-0fa7f600-c004-11eb-897b-6bbe22ec4d35.JPG)


![Capture6](https://user-images.githubusercontent.com/60011091/120019417-0d469b80-c006-11eb-9e22-26c943b2fb59.JPG)


![Capture7](https://user-images.githubusercontent.com/60011091/120019809-8219d580-c006-11eb-8998-f876fe49907e.JPG)


![Capture8](https://user-images.githubusercontent.com/60011091/120020022-ce651580-c006-11eb-9591-7c2ba233c6b9.JPG)


![Capture9](https://user-images.githubusercontent.com/60011091/120020131-f3598880-c006-11eb-9742-f6c6c835e7bd.JPG)


![Capture10](https://user-images.githubusercontent.com/60011091/120021034-2c462d00-c008-11eb-88be-e0dccef19b6f.JPG)


![Capture11](https://user-images.githubusercontent.com/60011091/120021160-526bcd00-c008-11eb-880c-af66a429ae95.JPG)


#### Design


![Capture12](https://user-images.githubusercontent.com/60011091/120021523-cc03bb00-c008-11eb-97f0-eac9dbb78b88.JPG)


sky130_fd_sc_hd__o21ai_1 in netlist visualization has 3 inputs and 1 output as it has 2 input OR  gate into first input of 2input NAND gate. sky130_fd_sc_hd is a high density digital standard cell contributed Skywater foundry.


## Day-2 Timing libs  Hierarchy versus flat synthesis and efficient flop styles

### .lib file lab 
![Capture13](https://user-images.githubusercontent.com/60011091/120023408-5c42ff80-c00b-11eb-9695-e9d3daf567db.JPG)


![Capture14](https://user-images.githubusercontent.com/60011091/120023428-62d17700-c00b-11eb-9f33-de5ab2ef58a3.JPG)


![Capture15](https://user-images.githubusercontent.com/60011091/120023495-7aa8fb00-c00b-11eb-960e-ab05706f992b.JPG)


sky130_fd_sc_hd__tt_025c_1v80.lib --> has 025c as temperature parameter, 1v80 as voltage parameter and tt which is a typical process parameter.


![Capture18](https://user-images.githubusercontent.com/60011091/120025121-d83e4700-c00d-11eb-8e61-636ed6b56637.JPG)


### Hierarchy vs flat Synthesis lab 

Hierarchy Synthesis

![Capture16](https://user-images.githubusercontent.com/60011091/120024686-2ef75100-c00d-11eb-98bc-2082e617716f.JPG)


#### Synthesis 


    $ yosys
    yosys> read_liberty -lib  ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> read_verilog multiple_module.v
    yosys> synth -top multiple_module
    yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> show multiple_modules
    yosys> write_verilog -noattr multiple_modules_hier.v
    yosys> show



![Capture17](https://user-images.githubusercontent.com/60011091/120024695-30c11480-c00d-11eb-9893-60a9777b6f6d.JPG)


![Capture19](https://user-images.githubusercontent.com/60011091/120025454-526ecb80-c00e-11eb-9062-72e7be2122c8.JPG)


![Capture20](https://user-images.githubusercontent.com/60011091/120025621-9792fd80-c00e-11eb-9f28-ec621cad920f.JPG)



![Capture21](https://user-images.githubusercontent.com/60011091/120025794-d6c14e80-c00e-11eb-88f9-8d5bc2e02420.JPG)


![Capture22](https://user-images.githubusercontent.com/60011091/120025891-f48eb380-c00e-11eb-9464-2859ee503b48.JPG)


![Capture23](https://user-images.githubusercontent.com/60011091/120026094-30c21400-c00f-11eb-9cba-28fe3515c2cd.JPG)


#### Design

![Capture24](https://user-images.githubusercontent.com/60011091/120026330-8ac2d980-c00f-11eb-9822-41a2a49d049e.JPG)

##### Hierarchy file

      yosys> !gedit multiple_modules_hier.v

![image](https://user-images.githubusercontent.com/60011091/120103768-e35cb880-c16e-11eb-98ef-19a7517cd75f.png)



##### Flat Synthesis 

      yosys> write_verilog -noattr multiple_modules_flat.v

![Capture27](https://user-images.githubusercontent.com/60011091/120027495-0e30fa80-c011-11eb-9812-65ac466afb91.JPG)

      yosys> !gedit multiple_modules_flat.v 

![Capture28](https://user-images.githubusercontent.com/60011091/120027691-4fc1a580-c011-11eb-8bb7-1f36dd655bbf.JPG)


##### Submodules

    $ yosys
    yosys> read_liberty -lib  ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> read_verilog multiple_module.v
    yosys> synth -top multiple_module
    yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> show multiple_modules
    yosys> write_verilog -noattr multiple_modules_hier.v
    yosys> show


![Capture29](https://user-images.githubusercontent.com/60011091/120028253-1178b600-c012-11eb-8b6f-70770b408aed.JPG)


![Capture30](https://user-images.githubusercontent.com/60011091/120028309-25241c80-c012-11eb-905a-b8b2d2a14be0.JPG)


![Capture31](https://user-images.githubusercontent.com/60011091/120028566-76341080-c012-11eb-9ccf-0748ec1895ba.JPG)


![Capture32](https://user-images.githubusercontent.com/60011091/120028549-703e2f80-c012-11eb-9e4f-d255969134d5.JPG)



#### Why Flops and Flops Designs 


![image](https://user-images.githubusercontent.com/60011091/120029004-1db14300-c013-11eb-9a98-e2900ac64a09.png)


The above image shows the comparison Asynchronous reset, Asynchronous set , Synchronous reset and Synchronous reset.


### Lab for Flop styles


Using Simulator and Waveform viewer


##### Asynchronous reset

      $ iverilog dff_asyncres.v tb_dff_asyncres.v
      $ ./a.out
      $ gtkwave tb_dff_asynres.vcd

![Capture34](https://user-images.githubusercontent.com/60011091/120029558-e727f800-c013-11eb-9a8e-2e69f1e86435.JPG)


![Capture35](https://user-images.githubusercontent.com/60011091/120029806-35d59200-c014-11eb-9056-f23897ae7033.JPG)


##### Asynchronous set

     $ iverilog dff_async_set.v tb_dff_async_set.v
     $ ./a.out
     $ gtkwave tb_dff_async_set.vcd
                    


![Capture36](https://user-images.githubusercontent.com/60011091/120030107-a7154500-c014-11eb-9c81-65c59975dda8.JPG)


![Capture37](https://user-images.githubusercontent.com/60011091/120030248-da57d400-c014-11eb-8e0d-5fa73442be08.JPG)


##### Synchronous reset

      $ iverilog dff_syncres.v tb_dff_syncres.v
      $ ./a.out
      $ gtkwave tb_dff_synres.vcd


Using Simulator and Waveform viewer

![Capture38](https://user-images.githubusercontent.com/60011091/120030551-3e7a9800-c015-11eb-8018-7beaaf449fbe.JPG)


![Capture39](https://user-images.githubusercontent.com/60011091/120030736-7681db00-c015-11eb-9e40-1346fcf12382.JPG)



##### Using Synthesizer for Asynchronous reset

    $ yosys
    yosys> read_liberty -lib  ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> read_verilog dff_asynres.v
    yosys> synth -top dff_asynres
    yosys> dfflibmap -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> show

![Capture40](https://user-images.githubusercontent.com/60011091/120031276-396a1880-c016-11eb-8f0e-2e77df970772.JPG)


![Capture42](https://user-images.githubusercontent.com/60011091/120031373-5999d780-c016-11eb-9ee7-169938a1988e.JPG)


![Capture41](https://user-images.githubusercontent.com/60011091/120031223-26efdf00-c016-11eb-969c-f911f6101c66.JPG)




![Capture43](https://user-images.githubusercontent.com/60011091/120031797-e5abff00-c016-11eb-8a98-ce60607a1bd5.JPG)


![Capture44](https://user-images.githubusercontent.com/60011091/120031970-27d54080-c017-11eb-96b3-b5f9f030a33d.JPG)


![Capture45](https://user-images.githubusercontent.com/60011091/120032098-52bf9480-c017-11eb-8104-3f7e8c9ed2ea.JPG)


### Interesting Optimizations

     $ gedit mul_*.v


![Capture46](https://user-images.githubusercontent.com/60011091/120056558-b323f580-c05a-11eb-8dfc-070a2d07193a.JPG)


![Capture47](https://user-images.githubusercontent.com/60011091/120056581-d2bb1e00-c05a-11eb-80c6-a98560b97fd6.JPG)


![Capture48](https://user-images.githubusercontent.com/60011091/120056613-0433e980-c05b-11eb-954d-49ea21be1ea4.JPG)


##### Synthesis 

    $ yosys
    yosys> read_liberty -lib  ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> read_verilog mult_2.v
    yosys> synth -top mult2
    yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> show


![Capture49](https://user-images.githubusercontent.com/60011091/120056712-b370c080-c05b-11eb-9510-8b7c29d53e4c.JPG)


![Capture50](https://user-images.githubusercontent.com/60011091/120056780-12363a00-c05c-11eb-84a5-dcd8631ab7f2.JPG)


![Capture51](https://user-images.githubusercontent.com/60011091/120056796-2aa65480-c05c-11eb-9459-5df27bb118a8.JPG)



![Capture52](https://user-images.githubusercontent.com/60011091/120056840-5e817a00-c05c-11eb-83b7-ae71f8596c17.JPG)


##### Design 


![Capture53](https://user-images.githubusercontent.com/60011091/120056868-8c66be80-c05c-11eb-9c52-944f50cd174d.JPG)


## Day-3 Combinational and Sequential Optimizations


### Combinational Optimizations


Logics are squeezed to obtain the most optimized design in terms of Area, Power savings



#### Methods for Combinational  Optimizations


1) Constant propagation 
-Direct optimization

We will be taking an example, Y= ((AB)+ C)'.

If we take A=0 as input, we get Y= C'
So, clearly we see that we directly need inverter to invert input C.


2) Boolean Logic Optimization 

-K map 
-Quine McKluskey

Here we take an example, assign y= a?(b?c:(c?a:0)):!c), this statement uses  ternary operator and this one is a mux kind of expression.
If a=1, it will take b?c:(c?a:0) expression or else a=0 it will take !c as the expression.
If b=1, it will take c's value or else b=0 it will take c?a:0 expression.
if c=1, it will take a's value or else c=0 it will take the value as '0'. 

The overall MUX expression will be Y=  ((ac+c'0). b'+bc).a+ a'c'    (Since c'.0=0)
                                  Y=  ((acb'+bc).a + a'c'
                                   Y= a'c' +acb'+abc 
                                   Y= a'c' +ac(b'+b)     (b'+b=1)
                                   Y= a'c + ac ie Y= a xor c
                                   
                                   
                                   
### Sequential Optimizations


#### Methods for Sequential  Optimizations

1) Basic
 
-Sequential constant propagation

![image](https://user-images.githubusercontent.com/60011091/120106169-b1048880-c179-11eb-9b08-9070f0996fa2.png)

Here in this circuit even if there is a reset or not the Q value value is going to be 0. So Y value is always 1 as it has nand gate inverting the value of Q.

2)Advanced  
-State optimization ( optimization of unused states)
-Retiming (Splitting the logic more equally to get a better effective frequency for a sequential circuit)
-Sequential Logic cloning (floor plan aware synthesis)


### Lab for Combinational Optimizations

     $ ls *opt*
     $ ls *opt_check*

![Capture54](https://user-images.githubusercontent.com/60011091/120061083-145ac180-c079-11eb-9c58-5a438ee40fad.JPG)

Here we will be taking first file opt_check module where we have assign y= a?b:0, which is a mux so at a=1, y will take b's values, but at a=0, y will take 0 as its value.

    $ yosys
    yosys> read_liberty -lib  ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> read_verilog opt_check.v
    yosys> synth -top opt_check
    yosys> opt_clean -purge
    yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> show


![Capture56](https://user-images.githubusercontent.com/60011091/120061922-16bf1a80-c07d-11eb-9cac-3dbd5890260b.JPG)

![Capture57](https://user-images.githubusercontent.com/60011091/120061957-3d7d5100-c07d-11eb-85ff-f6d3433e536a.JPG)

![Capture58](https://user-images.githubusercontent.com/60011091/120062013-7f0dfc00-c07d-11eb-97b4-759317a69240.JPG)

![Capture59](https://user-images.githubusercontent.com/60011091/120062043-a1077e80-c07d-11eb-9f5b-a41d7f00e3b9.JPG)

#### Design

![Capture60](https://user-images.githubusercontent.com/60011091/120062096-e1ff9300-c07d-11eb-8b08-2368fcff286b.JPG)



Here we will be taking second file opt_check2 module where we have assign y= a?1;b, which is a mux so at a=1, y will take 1, but at a=0, y will take b's value.


    $ yosys
    yosys> read_liberty -lib  ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> read_verilog opt_check2.v
    yosys> synth -top opt_check2
    yosys> opt_clean -purge
    yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> show

![Capture61](https://user-images.githubusercontent.com/60011091/120062648-e37e8a80-c080-11eb-8cfa-82775f19018b.JPG)

![Capture62](https://user-images.githubusercontent.com/60011091/120062740-3eb07d00-c081-11eb-86a2-8b3c9eb6d430.JPG)

![Capture63](https://user-images.githubusercontent.com/60011091/120062756-51c34d00-c081-11eb-9d17-5c5141baff12.JPG)

![Capture64](https://user-images.githubusercontent.com/60011091/120062784-8505dc00-c081-11eb-94e4-c2b8b91cce40.JPG)



### Lab for Sequential Optimizations


##### dff_const2


     $ iverilog dff_const2.v tb_dff_const2.v
     $ ./a.out
     $ gtkwave tb_dff_const2.vcd

    

![Capture65](https://user-images.githubusercontent.com/60011091/120063008-af0bce00-c082-11eb-8421-ce3623d80f16.JPG)

![Capture65](https://user-images.githubusercontent.com/60011091/120063135-5be64b00-c083-11eb-962c-8b8fa0067b9e.JPG)



![Capture66](https://user-images.githubusercontent.com/60011091/120063162-75879280-c083-11eb-884f-e3f4e6520d00.JPG)

![Capture69](https://user-images.githubusercontent.com/60011091/120063891-1592eb00-c087-11eb-8550-7be69f41940a.JPG)

![image](https://user-images.githubusercontent.com/60011091/120063938-5854c300-c087-11eb-88a0-843af2713ad9.png)


##### Synthesis

    $ ls *dff*const*
    $ gedit dff_const1.v o dff_const2.v
    $ yosys
    yosys> read_liberty -lib  ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> read_verilog opt_check2.v
    yosys> synth -top opt_check2
    yosys> opt_clean -purge
    yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> show


![Capture76](https://user-images.githubusercontent.com/60011091/120064872-14b08800-c08c-11eb-9468-8deca70722e9.JPG)


![Capture77](https://user-images.githubusercontent.com/60011091/120064869-0ebaa700-c08c-11eb-9ede-15414dc67fb9.JPG)


#### Design

![Capture78](https://user-images.githubusercontent.com/60011091/120064937-7a9d0f80-c08c-11eb-87b2-e59ecd7ad426.JPG)


##### dff_const1

     $ iverilog dff_const1.v tb_dff_const1.v
     $ ./a.out
     $ gtkwave tb_dff_const1.vcd
     
     
![Capture67](https://user-images.githubusercontent.com/60011091/120063291-0a8a8b80-c084-11eb-9b40-2c187432abab.JPG)

![Capture68](https://user-images.githubusercontent.com/60011091/120063462-e8453d80-c084-11eb-88a5-2b511f59acec.JPG)




##### Synthesis


    $ yosys
    yosys> read_liberty -lib  ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> read_verilog opt_check2.v
    yosys> synth -top opt_check2
    yosys> opt_clean -purge
    yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> show


![Capture71](https://user-images.githubusercontent.com/60011091/120064324-28a6ba80-c089-11eb-8125-353dab4c3d9d.JPG)

![Capture72](https://user-images.githubusercontent.com/60011091/120064398-8dfaab80-c089-11eb-9730-c77d5c3c2f1c.JPG)

![Capture73](https://user-images.githubusercontent.com/60011091/120064463-e5008080-c089-11eb-95a2-ccb329020724.JPG)

![Capture74](https://user-images.githubusercontent.com/60011091/120064499-0fead480-c08a-11eb-9c30-0618d420e1c1.JPG)

#### Design

![Capture75](https://user-images.githubusercontent.com/60011091/120064527-3e68af80-c08a-11eb-8407-2d62f450cb8e.JPG)




### Lab for Sequential Optimizations for unused inputs


#### Simulation and waveform viewer 

    $ gedit counter_opt.v
    $ iverilog counter_opt.v tb_counter_opt.v
    $ ./a.out
    $ gtkwave tb_counter_opt.vcd
   
   


![Capture79](https://user-images.githubusercontent.com/60011091/120065562-80482480-c08f-11eb-9bf1-2034ab11bd58.JPG)

![Capture80](https://user-images.githubusercontent.com/60011091/120065611-c8674700-c08f-11eb-9266-8fdb62792f4c.JPG)


#### Sythesis 

    $ yosys
    yosys> read_liberty -lib  ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> read_verilog counter_opt.v
    yosys> synth -top counter_opt
    yosys> dfflibmap -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> show

![Capture81](https://user-images.githubusercontent.com/60011091/120065772-af12ca80-c090-11eb-8dbd-9e3ca2515f74.JPG)

![Capture82](https://user-images.githubusercontent.com/60011091/120065851-1fb9e700-c091-11eb-82b8-71ce5a0eee99.JPG)

![Capture83](https://user-images.githubusercontent.com/60011091/120065880-40823c80-c091-11eb-9fbf-256e002c2035.JPG)

![Capture84](https://user-images.githubusercontent.com/60011091/120065916-6d365400-c091-11eb-9fa2-14b3c2f76655.JPG)

#### Design

![Capture85](https://user-images.githubusercontent.com/60011091/120065943-97881180-c091-11eb-93f0-edebfd1b5d30.JPG)



## DAY-4 Gate Level Synthesis  Synthesis Simulation mismatch and Blocking Non blocking statements

 ### GLS

Here we are going to run the tesbench along with netlist as DUT (Design under Test).
Netlist and RTL code are one and the same as we are going to use the same testbench for the design 
We need GLS to verify the correctness of the design after synthesis and also for ensuring the timing of the design is met.
If the Gate level models are delay annotated, GLS can be used for timing validation.


#### GLS using iverilog 

![Untitled Workspace](https://user-images.githubusercontent.com/60011091/120066929-8ee60a00-c096-11eb-82d1-95bd7ed6029e.png)

### Synthesis Simulation Mismatches

This can happen because of following conditions as listed below:

1) Missing sensitivity list

Here we will be taking an example code 

![Capture86](https://user-images.githubusercontent.com/60011091/120067266-3879cb00-c098-11eb-952b-c42f9004ec05.JPG)

Here we see that whenever 'sel' is changing 'y' will also be changing. 
The always block statement gets evaluated only when 'sel' is changing and so always block is not sensitive to either i1 or i2 activities because of which we will not be getting Y output based on changes in i0 and i1. So this circuit behaves like a latch 

So, the solution to this problem is the below image showing us the code.

![Capture87](https://user-images.githubusercontent.com/60011091/120067511-b094c080-c099-11eb-8bd6-425570fdb478.JPG)
Here the always block gets evaluated for 'sel', 'i0' and 'i1'. So now we will be getting the exact output as we had expected.


2) Blocking versus non blocking assignments

Inside always block 

#### a) = ---> Blocking
- Executes the statements in the order it is written and so the first statement is evaluated before the second statement

#### b) <= ---> Non Blocking
- Executes all the RHS when the always block is entered and assigned to LHS. So in other words, this assignments does parallel evaluation.

#### Caveats in Blocking Statements example 


![Capture88](https://user-images.githubusercontent.com/60011091/120068096-990b0700-c09c-11eb-8dad-a54cfd7dbe46.JPG)
![Capture89](https://user-images.githubusercontent.com/60011091/120068178-fdc66180-c09c-11eb-86f3-a09d494c812b.JPG)

Comparing the above images with code the first images shows the correct code 
But in the second image in the third begin statement instead of q=qo then q0=d but we've q0=d followed by q=q0 so by the time q0 is assigned to q, q0 will be already having the value of d that means there is only one flip flop instead of two in the 1st image of this section.

The second image code problem can be fixed by using non blocking statements as shown below:

![Capture90](https://user-images.githubusercontent.com/60011091/120068420-3adf2380-c09e-11eb-928e-218628c5f6f9.JPG)


We take a different example to understand the problem more clearly

![Capture91](https://user-images.githubusercontent.com/60011091/120068647-5bf44400-c09f-11eb-923b-ce21a9860e22.JPG)

Here in the above image  has y=q0&c and q0=a|b so q0 will be taking the previous value to evaluate y then a|b is assigned to q0. So this code mimic a delay or a flip flop 

Solution to this problem is the below image 

![Capture92](https://user-images.githubusercontent.com/60011091/120068776-0cfade80-c0a0-11eb-8001-3a75780f8ffc.JPG)

### Lab for GLS Synthesis Simulation Mismatch

     

![Capture93](https://user-images.githubusercontent.com/60011091/120069040-716a6d80-c0a1-11eb-9b12-a4bc6133f156.JPG)

![Capture94](https://user-images.githubusercontent.com/60011091/120069064-91019600-c0a1-11eb-8207-03c76722fa11.JPG)

![Capture95](https://user-images.githubusercontent.com/60011091/120069162-11c09200-c0a2-11eb-9545-53b38ab99deb.JPG)

##### Simulation and Waveform Viewer

    $ iverilog ternary_operator_mux.v tb_ternary_operator_mux.v
    $ ./a.out
    $ gtkwave tb_ternary_operator_mux.vcd

![Capture96](https://user-images.githubusercontent.com/60011091/120069346-2a7d7780-c0a3-11eb-8220-4bae1c506581.JPG)

![Capture97](https://user-images.githubusercontent.com/60011091/120069453-aecffa80-c0a3-11eb-9fcc-2a27e9374e83.JPG)

##### Synthesis
    
    $ yosys
    yosys> read_liberty -lib  ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> read_verilog ternary_operator_mux.v
    yosys> synth -top ternary_operator_mux
    yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> write_verilog -noattr ternary_operator_mux_net.v
    yosys> show

![Capture98](https://user-images.githubusercontent.com/60011091/120069595-4cc3c500-c0a4-11eb-9d89-c657dc38cd16.JPG)

![Capture99](https://user-images.githubusercontent.com/60011091/120069685-cfe51b00-c0a4-11eb-8e8c-4d1705b5ab12.JPG)

![Capture100](https://user-images.githubusercontent.com/60011091/120069843-9cef5700-c0a5-11eb-9a32-7b017a20e559.JPG)

![image](https://user-images.githubusercontent.com/60011091/120069881-ca3c0500-c0a5-11eb-9bbe-4025b42de784.png)

#### Design 

![Capture102](https://user-images.githubusercontent.com/60011091/120069915-05d6cf00-c0a6-11eb-8ae8-82a67d194b0b.JPG)


##### GLS Simulation 

    $ iverilog ../my_lib/verilog_model/primitive.v ../my_lib/verilog_model/sky130_fd_sc_hd.v ternary_operator_mux_net.v tb_ternary_operator_mux.v
    $ ./a.out
    $ gtkwave tb_ternary_operator_mux.vcd


![Capture103](https://user-images.githubusercontent.com/60011091/120070281-4d118f80-c0a7-11eb-9ced-6f5136dccab6.JPG)

![Capture104](https://user-images.githubusercontent.com/60011091/120070382-e0e35b80-c0a7-11eb-8068-f2fc98742221.JPG)


#### Bad Mux Example


![Capture94](https://user-images.githubusercontent.com/60011091/120069064-91019600-c0a1-11eb-8207-03c76722fa11.JPG)

##### Simulation

    $ iverilog bad_mux.v tb_bad_mux.v
    $ ./a.out
    $ gtkwave tb_bad_mux.vcd

![Capture105](https://user-images.githubusercontent.com/60011091/120070515-8dbdd880-c0a8-11eb-97b2-5f2168cf2a9b.JPG)

![Capture106](https://user-images.githubusercontent.com/60011091/120070570-ce1d5680-c0a8-11eb-8061-2aeb8fc11e7b.JPG)

##### Synthesis 

    $ yosys
    yosys> read_liberty -lib  ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> read_verilog bad_mux.v
    yosys> synth -top bad_mux
    yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> write_verilog -noattr bad_mux_net.v
    yosys> show

![Capture107](https://user-images.githubusercontent.com/60011091/120070740-a4186400-c0a9-11eb-8a26-37b1e55ff00b.JPG)

![Capture108](https://user-images.githubusercontent.com/60011091/120070822-f8234880-c0a9-11eb-9ae8-7f2b818bd337.JPG)

![Capture109](https://user-images.githubusercontent.com/60011091/120070889-55b79500-c0aa-11eb-8985-61f026007488.JPG)



###### GLS simulation 


    $ iverilog ../my_lib/verilog_model/primitive.v ../my_lib/verilog_model/sky130_fd_sc_hd.v bad_mux_net.v tb_bad_mux.v
    $ ./a.out
    $ gtkwave tb_bad_mux.vcd

![Capture110](https://user-images.githubusercontent.com/60011091/120071048-06259900-c0ab-11eb-8aa5-6179f6f770ff.JPG)


###### Comparison

![Capture106](https://user-images.githubusercontent.com/60011091/120070570-ce1d5680-c0a8-11eb-8061-2aeb8fc11e7b.JPG)

![Capture111](https://user-images.githubusercontent.com/60011091/120071170-a4b1fa00-c0ab-11eb-8c5c-99ff7fdde7ce.JPG)




### Lab for Synthesis Simulation Mismatch for blocking statements

![Capture112](https://user-images.githubusercontent.com/60011091/120071837-8dc0d700-c0ae-11eb-9e59-da6b4d3533f4.JPG)

The above image d= x &c and x = a|b, here we have to take previous value of x for evaluating d as if x is to be a flopped output in simulation


    $ gedit blocking_caveat.v
    $ iverilog blocking_caveat.v tb_blocking_caveat.v
    $ ./a.out
    $ gtkwave tb_blocking_caveat.vcd


![Capture113](https://user-images.githubusercontent.com/60011091/120072100-a1207200-c0af-11eb-9522-950b98274211.JPG)

![Capture114](https://user-images.githubusercontent.com/60011091/120072169-02e0dc00-c0b0-11eb-8981-2d1cf5d092b2.JPG)

##### Synthesis 

    $ yosys
    yosys> read_liberty -lib  ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> read_verilog blocking_caveat.v
    yosys> synth -top blocking_caveat
    yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> write_verilog -noattr blocking_caveat_net.v
    yosys> show


![Capture115](https://user-images.githubusercontent.com/60011091/120072252-85699b80-c0b0-11eb-964e-3f237a9b15ee.JPG)

![Capture116](https://user-images.githubusercontent.com/60011091/120072296-c8c40a00-c0b0-11eb-8c3c-9b6fe412068a.JPG)

![Capture117](https://user-images.githubusercontent.com/60011091/120072352-1e001b80-c0b1-11eb-9412-6c500ddf5b99.JPG)

![Capture118](https://user-images.githubusercontent.com/60011091/120072390-56075e80-c0b1-11eb-8857-c37bde65ffd6.JPG)


##### GLS Simulation

    $ iverilog ../my_lib/verilog_model/primitive.v ../my_lib/verilog_model/sky130_fd_sc_hd.v blocking_caveat_net.v tb_blocking_caveat.v
    $ ./a.out
    $ gtkwave tb_blocking_caveat.vcd


![Capture119](https://user-images.githubusercontent.com/60011091/120072537-08d7bc80-c0b2-11eb-8a26-717b70daad95.JPG)

##### Comparison
![Capture114](https://user-images.githubusercontent.com/60011091/120072169-02e0dc00-c0b0-11eb-8981-2d1cf5d092b2.JPG)

![Capture120](https://user-images.githubusercontent.com/60011091/120072640-7e438d00-c0b2-11eb-89de-0a5138995f82.JPG)


## Day-5 If Case For Loop and for Generate statements

###  If statements

If statements are mainly used to create priority logic. These statements are used inside alaways block. Variables used in if statements are register variables.

The syntax and structure of If statement is given below

                        if <condition 1>
                        begin
                        ---------
                        ---------
                        ---------
                        end
                        else if <condition 2>
                        begin
                        ---------
                        ---------
                        ---------
                        end
                        else if <condition 3>
                        begin
                        ---------
                        ---------
                        ---------
                        end
                        else 
                        begin
                        ---------
                        ---------
                        ---------
                        end
 
The above structure depending on the number of if-else if statements we can map these statements in the form of hardware circuit that is a mux with conditions. 
                        
 #### Dangers of If statement 
 
 Incomplete If statements can cause inferred latches and this is particularly a bad coding style. The example is shown below:
 
 
 if (condt1)
     y=a;
 else if (condt2)  
     y=b;
     
     
 If we leave the code incomplete like this if any of the conditions are not satisfied it will automatically try to latch as we have not provided the else statement in the above example. This latch condition is called inferred latch condition when incomplete if statement is used.
 
 
 There are cases where we use incomplete if statements say for examplwe use it in counters then the incomplete if statements looks like this,
 
 always @ (posedge clk, posedge reset)
 begin 
    if(reset)
       count<=3'b000;
    else if (en)
       count<=count+1;
 end
 
 If there is no count value the circuit will automatically latches to store previous avlue to be used in the next iteration. Since counters are sequential circuits this latching proves to be useful and so this is one of the exception cases of incomplete if statements.
 
 
 

###  Case statements

Case statements are used inside always block. Variables used in case statements are register variables. Example for case statement is shown below:

       reg y;
       always @(*)
       begin
       case(sel)
           2'b00: begin
              ---------
              ---------
                  end
           2'b01: begin
              ---------
              ---------
                  end
       ---------------
       ---------------
       ---------------
           default: -----------
           --------------------
      endcase
      end


#### Caveats in case statements


##### Incomplete case statements

This incomplete case statements also causes inferred latches just as in incomplete if statements. The example is shown below:


    reg y;
    always @(*)
    begin
     case(sel)
       2'b00: begin
              ---------
              ---------
              end
       2'b01: begin
              ---------
              ---------
              end
     endcase
    end  
       
Since, we have not told what's to be done after 2'b01 condition, the hardware will map the rest as a latch to retain previous values.       
          
 Solution to this problem is by adding default case statement to aviod latch up condition. 
 
 
##### Partial assignment in case statement 


    reg y;
    always @(*)
    begin
    case(sel)
       2'b00: begin
              x=a;
              y=b;
              end
       2'b01: begin
              x=c;
              end
       default: begin
              x=d;
              y=b;
              end         
    endcase
    end  

Here we see that in 2'b01 we have incomplete assignments ie x is assigned 'c' buy y value is not known to us due to this again latch up happens to retain the previous value of y ie it take y=b from 2'b00 condition. 

##### If we take an example like shown below, let's observe what happens next...

     reg y;
     always @(*)
     begin
     case(sel)
       2'b00: begin
              ---------
              ---------
              end
       2'b01: begin
              ---------
              ---------
              end
       2'b10: begin
              ---------
              ---------
              end       
       2'b1?: begin
              ---------
              ---------
              end      
              
     endcase
    end  

Here we will be getting unpredictable output as case statements are executed one after the other escpecially reaching the last condition statement 2'b1?: where we say our MSB is 1 bur lsb can be anything from 1 or 0 ans we can predict the exact value of the final outputs.

This is an overlapping case statements.

### Lab for Incomplete If statements

We will be taking an example, incomp_if file

![Capture121](https://user-images.githubusercontent.com/60011091/120091136-cd76d580-c125-11eb-8bba-89b9444ddf59.JPG)


#### Simulation and waveform viewer

    $ iverilog incomp_if.v tb_incomp_if.v
    $ ./a.out
    $ gtkwave tb_incomp_if.vcd

![Capture122](https://user-images.githubusercontent.com/60011091/120091567-db2e5a00-c129-11eb-8b6a-1f9c6f12fcf5.JPG)

![Capture123](https://user-images.githubusercontent.com/60011091/120091242-ea5fd880-c126-11eb-86dd-4a06ff8bdfc5.JPG)

#### Synthesis 

    $ yosys
    yosys> read_liberty -lib  ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> read_verilog incomp_if.v
    yosys> synth -top incomp_if
    yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> show


![Capture124](https://user-images.githubusercontent.com/60011091/120091340-d8326a00-c127-11eb-9864-066676d79e62.JPG)

![Capture125](https://user-images.githubusercontent.com/60011091/120091369-2a738b00-c128-11eb-872e-6f20c321f281.JPG)

![Capture126](https://user-images.githubusercontent.com/60011091/120091385-55f67580-c128-11eb-8941-b58d39abe83a.JPG)


#### Design 

![Capture127](https://user-images.githubusercontent.com/60011091/120091407-7b837f00-c128-11eb-89fc-9f8a375f417b.JPG)



We will be taking another example, incomp_if2

![Capture128](https://user-images.githubusercontent.com/60011091/120091510-622f0280-c129-11eb-96b3-07096ad36b11.JPG)

#### Simulation and waveform viewer

    $ iverilog incomp_if2.v tb_incomp_if2.v
    $ ./a.out
    $ gtkwave tb_incomp_if2.vcd 

![Capture129](https://user-images.githubusercontent.com/60011091/120095229-69163f00-c142-11eb-827d-9875b505d903.JPG)

![Capture130](https://user-images.githubusercontent.com/60011091/120091654-ed5cc800-c12a-11eb-8e8f-3841e7a12a18.JPG)


#### Synthesis 

    $ yosys
    yosys> read_liberty -lib  ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> read_verilog incomp_if2.v
    yosys> synth -top incomp_if2
    yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> show

![Capture131](https://user-images.githubusercontent.com/60011091/120091699-43ca0680-c12b-11eb-8384-9521e8ed6f24.JPG)
![Capture132](https://user-images.githubusercontent.com/60011091/120091830-25b0d600-c12c-11eb-8ca5-ccfbee87f8c8.JPG)
![Capture133](https://user-images.githubusercontent.com/60011091/120091847-424d0e00-c12c-11eb-9503-22a08f66ba8c.JPG)


#### Design 
![Capture134](https://user-images.githubusercontent.com/60011091/120091866-6e688f00-c12c-11eb-9106-77d37153d89e.JPG)


### Lab for Incomplete case statements

We will be taking an example of complete case statement file

![Capture135](https://user-images.githubusercontent.com/60011091/120095040-433c6a80-c141-11eb-9187-a056d82c591d.JPG)

#### Simulation and waveform viewer

    $ iverilog comp_case.v tb_comp_case.v
    $ ./a.out
    $ gtkwave tb_comp_case.vcd 

![Capture136](https://user-images.githubusercontent.com/60011091/120095132-d2498280-c141-11eb-9a7a-5e73edfba553.JPG)
![Capture137](https://user-images.githubusercontent.com/60011091/120095239-77fcf180-c142-11eb-9fbf-638b675a8268.JPG)

#### Synthesis 

    $ yosys
    yosys> read_liberty -lib  ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> read_verilog comp_case.v
    yosys> synth -top comp_case
    yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> show
    
![image](https://user-images.githubusercontent.com/60011091/120095340-1be69d00-c143-11eb-9088-281423fb4dba.png)
![Capture139](https://user-images.githubusercontent.com/60011091/120095358-3ae52f00-c143-11eb-84b9-5745c1476b4a.JPG)
![Capture140](https://user-images.githubusercontent.com/60011091/120095383-5c461b00-c143-11eb-8698-0e2f4c872a74.JPG)

#### Design 
![Capture141](https://user-images.githubusercontent.com/60011091/120095442-9e6f5c80-c143-11eb-8dde-4b026014a825.JPG)



We will be taking another example, incomplete statement file

![Capture142](https://user-images.githubusercontent.com/60011091/120095512-04f47a80-c144-11eb-8250-f1748afa14ff.JPG)


#### Simulation and waveform viewer
     
    $ iverilog incomp_case.v tb_incomp_case.v
    $ ./a.out
    $ gtkwave tb_incomp_case.vcd 

![Capture143](https://user-images.githubusercontent.com/60011091/120095580-53a21480-c144-11eb-819d-3f940e974a29.JPG)

![Capture144](https://user-images.githubusercontent.com/60011091/120095689-e642b380-c144-11eb-9e1c-0fc3aa7ae0e8.JPG)


#### Synthesis 

    $ yosys
    yosys> read_liberty -lib  ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> read_verilog incomp_case.v
    yosys> synth -top incomp_case
    yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> show

![Capture145](https://user-images.githubusercontent.com/60011091/120095703-f2c70c00-c144-11eb-9358-e375bd8e7513.JPG)

![Capture146](https://user-images.githubusercontent.com/60011091/120095716-18541580-c145-11eb-990f-4b8d57adb964.JPG)
![Capture147](https://user-images.githubusercontent.com/60011091/120095750-302b9980-c145-11eb-83f2-d8017211c4c6.JPG)


#### Design 

![Capture148](https://user-images.githubusercontent.com/60011091/120095787-73860800-c145-11eb-92ef-8f400a04147b.JPG)



###  For loop statements and For generate statements

Looping constructs uses for loop and  generate for loop statements


#### For loop statement
For loops can be used only inside always block. These loops can be used for evaluating expressions but not for instantaiating hardware.
Example we are taking is a 32:1 Mux is as shown below:

    integer i;
    always @(*)
    begin 
     for(i=0; i<32; i=i=1)
     begin
     if (i==sel)
       y= inp[i];    //Assuming that inp[32:0] bus is declared in the main module.
     end
    end     


#### Generate for loop statement

Generate for loop cannot be used inside always block but outside always block. Generate for loop is used in instantiating hardware.
Taking an example for generate foor loop as shown below

Suppose we need to instantiate and u_and( .a(), .b(), .y()) for 20 times it is not feasible to and u_and( .a(), .b(), .y()) this many times ie 

       and u_and( .a(), .b(), .y())
       and u_and( .a(), .b(), .y())
       and u_and( .a(), .b(), .y())
       ..................
       ..................
       ..................
       ..................
       Till 20th and gate instantiation

Here we use generate for loops to instantiate gates and smaller modules in main modules as my times we want.

     genvar i
     generate
      for (i=0; i,8; i=i+1) begin 
      and u_and( .a(a[i]), .b(b[i]), .y(y[i]));
      end
     end


      
### Lab for  For loop statement and For generate statements


We are taking an example where we are taking mux_generate file.

![Capture149](https://user-images.githubusercontent.com/60011091/120096767-ef368380-c14a-11eb-8093-c21ec2fd0c2c.JPG)


#### Simulation and waveform viewer

    $ iverilog mux_generate.v tb_mux_generate.v
    $ ./a.out
    $ gtkwave tb_mux_generate.vcd 


![Capture150](https://user-images.githubusercontent.com/60011091/120097488-53a71200-c14e-11eb-82b5-4ce60d6f095e.JPG)

![Capture151](https://user-images.githubusercontent.com/60011091/120097533-9b2d9e00-c14e-11eb-84ed-b51abcdcde77.JPG)


#### Synthesis

    $ yosys
    yosys> read_liberty -lib  ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> read_verilog mux_generate.v
    yosys> synth -top mux_generate
    yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> show


![Capture152](https://user-images.githubusercontent.com/60011091/120097751-e5fbe580-c14f-11eb-97a6-92557704c606.png)

![Capture156](https://user-images.githubusercontent.com/60011091/120097775-0330b400-c150-11eb-8227-0567721b9b5c.JPG)

![Capture157](https://user-images.githubusercontent.com/60011091/120097884-7d613880-c150-11eb-8ecc-72068f2f1d03.JPG)

![Capture158](https://user-images.githubusercontent.com/60011091/120097939-c9ac7880-c150-11eb-9ad6-55d05171a243.JPG)




#### Design 
![Capture159](https://user-images.githubusercontent.com/60011091/120097964-00828e80-c151-11eb-8d2e-0adf47931c43.JPG)




We are taking an example where we are taking rca.v file which is a ripple carry adder

![Capture160](https://user-images.githubusercontent.com/60011091/120098376-290b8800-c153-11eb-8ea7-d18ecbe7308f.JPG)


#### Simulation and waveform viewer

    $ iverilog fa.v rca.v tb_rca.v
    $ ./a.out
    $ gtkwave tb_rca.vcd 

![Capture161](https://user-images.githubusercontent.com/60011091/120098397-52c4af00-c153-11eb-8558-8f3a548c877c.JPG)

![Capture162](https://user-images.githubusercontent.com/60011091/120098533-0f1e7500-c154-11eb-95d6-5269c0bfccfd.JPG)


#### Synthesis
     
     $ yosys
    yosys> read_liberty -lib  ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> read_verilog fa.v rca.v
    yosys> synth -top rca
    yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
    yosys> write_verilog -noattr rca_net.v
    yosys> show
     
![Capture163](https://user-images.githubusercontent.com/60011091/120098777-6ec95000-c155-11eb-98b0-5f50edb6b0ce.JPG)


![Capture164](https://user-images.githubusercontent.com/60011091/120098773-683ad880-c155-11eb-81a6-0f61e0d32f50.JPG)


![Capture165](https://user-images.githubusercontent.com/60011091/120098785-7557c780-c155-11eb-8736-fdfff787838c.JPG)


![Capture166](https://user-images.githubusercontent.com/60011091/120099115-5a865280-c157-11eb-8771-b25756f7e4cd.JPG)


![Capture167](https://user-images.githubusercontent.com/60011091/120099175-cb2d6f00-c157-11eb-8492-281367e43c0b.JPG)





#### Design 

![Capture168](https://user-images.githubusercontent.com/60011091/120099325-7807ec00-c158-11eb-85b9-728ec237e0f5.JPG)


#### GLS Simulation

    $ iverilog ../my_lib/verilog_model/primitive.v ../my_lib/verilog_model/sky130_fd_sc_hd.v rca_net.v tb_rca.v
    $ ./a.out
    $ gtkwave tb_blocking_caveat.vcd
    
![Capture169](https://user-images.githubusercontent.com/60011091/120099488-51968080-c159-11eb-9a5b-1d352cc0416e.JPG)


#### Waveform Comparison 


![Capture162](https://user-images.githubusercontent.com/60011091/120098533-0f1e7500-c154-11eb-95d6-5269c0bfccfd.JPG)

![Capture171](https://user-images.githubusercontent.com/60011091/120099809-375da200-c15b-11eb-8e86-de3bc404a882.JPG)


Here we see that the waveform obtained in normal simulation and GLS simulation are the same.


By this, we have come to the end of 5 days workshop so by now I have sucessfully learnt theoretical and practical approach  on how to simulate, displaying waveform, synthesize, do gate level synthesis (netlist generation) and finally again display the waveforms to check the correctness of the design starting from smaller verilog codes to complex ones.



## Acknowledgements

1. Kunal Ghosh - Co-founder(VSD Corp. Pvt. Ltd)
2. Shon Taware - VSD Teaching Assistant
3. Chaitanya Bharathi 
