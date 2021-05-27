# Sky130 RTL Design and Synthesis Workshop

VSD Sky130 RTL was a five day workshop where I have learnt about the open source tools used in the VLSI Industry, timing liberties, hierarchical and flat synthesis concepts, optimization in both sequencial logic and combinational logic circuitry codes, GLS Blocking and non blocking statements and finally I have learnt about the optimization techniques used during synthesis of both logic and combinational logic circuitry codes . I will be briefly explaining about these topics daywise and I'll be cataloging my sail of these 5 days workshop.


![image](https://user-images.githubusercontent.com/60011091/119861437-04d26000-bf35-11eb-9515-85b05a1788d5.png)  ![image](https://user-images.githubusercontent.com/60011091/119867192-4108bf00-bf3b-11eb-9e46-4544afc0c9fa.png)


# DAY 1-  Verilog RTL design and Synthesis 

## RTL Simulation and Synthesis  

![image](https://user-images.githubusercontent.com/60011091/119868845-318a7580-bf3d-11eb-816c-7fef5d3e4eb0.png) 
![image](https://user-images.githubusercontent.com/60011091/119868918-46670900-bf3d-11eb-8873-ab8074c8f015.png)


Simulator is a tool for examining the correctness of your design. RTL design is the implementation of a given specification.The intent of specification needs to be verified by simulating the design. iverilog was used for simulation of a given design. Simulator looks for changes in the input signal and so if there is no change in the input signal of a design the output will reflect the same value given in the input signal.

Design can be an actual code or set of Verilog code whose functional intention is to meet a required specification and it should be a synthesizable verilog code. Design may have one or more  primary inputs and primary outputs depending on the design specifications.

![image](https://user-images.githubusercontent.com/60011091/119873702-6ea53680-bf42-11eb-9911-739fc9634018.png)


Testbench is an another verilog file which consists of instantiation of the top level module of a given design and it doesn't necessarily needed to be synthesizable code. But testbench doesn't really have primary inputs or any primary outputs.

![image](https://user-images.githubusercontent.com/60011091/119873898-ac09c400-bf42-11eb-955b-cf40b0a4b9bc.png)


![image](https://user-images.githubusercontent.com/60011091/119874652-7a452d00-bf43-11eb-904b-fc77dab90a3e.png)

The above image shows the flow of iverilog simulator whose inputs consist of design files and testbenches of the design and the value change dump (vcd) file is our output file.

![image](https://user-images.githubusercontent.com/60011091/119875139-0c4d3580-bf44-11eb-828d-fc0c7871261d.png)

In this image we see that the output file of iverilog that is our vcd file is sent as input to gtk wave which is a vcd waveform viewer where we can check the correctness of a particular design logic which can be a simple or a complex circuit or can be a combinational or sequential circuit designs.


## Setting up the Lab 


Here I'll be covering how we are going setup our lab server to simulate, view and synthesis the given specification of a design.

Initially we will be creating a VLSI directory using mkdir VLSI and then we cd into the directory using cd VLSI as shown below

![image](https://user-images.githubusercontent.com/60011091/119877385-98f8f300-bf46-11eb-8ece-f88d6dcbdde4.png)

Here we use ls commmand to list out all the files in that particular directory as shown in the above image. 

Before git cloning any repository in linux platform we can use sudo -i to enter root folder or by directly cloning that particular repository to the present folder and then we need to check whether git package is already installed if not install it using sudo apt-get install git








 


