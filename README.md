# Verilog Tutorials

This is a beginner friendly tutorial repository to learn verilog easily with all the basics that are required to get started for this language. Also, this repository is read only and is not currently being maintained by the author .

### Installation For Linux

* sudo apt-get update
* sudo apt-get install verilog
* sudo apt-get install gtkwave

### Introduction

Verilog is a hardware language which is a concurrent, case-sensitive and synthesizable language. Examples of such languages are VHDL( VHSIC(Very High Speed Integrated Circuit) HDL). It is vendor independent for example, Xilinx, Verywell etc.Full form verilog is __Verify Logic__. It is used for Digital ICs not for Analog ICs.It uses gate level design abstraction. It was made at Gateway Design Automation and now is IEEE 1364-2001 standard. HDL came to help with the verification of design of complex circuits that are in place. Also, logic synthesis tools can convert design to any fabrication technology. 

Now, verilog's basic building block is a module that provides information about input and output ports but hides internal implementation. 

### Levels of abstraction 

* Behavioral Level( Design of Algorithm ) : Algorithmic and performance oriented programs are written with it.
* Dataflow Level( Design of Equation ) : "assign" keyword is used for dataflow modelling. ex : assign c = a+b;
* Gate Level( Interconnection with Logic Gates ) : Circuits will be defined by logic gates. ex : and(output, input) etc.
* Switch Level( Implementation in terms of switches ) : Transistors either MOS or switches which conduct or are open. This style is complex and decreasing in popularity.

### Data Types

Two primary data-types are as follows :
* Nets : Connection between the components. Internal connection & is needed to be hidden from the user. Like, wire a;
* Registers : Store the data in variable. Like, reg a;

Other data-types are :  
* Vectors : nets and registers can be declared as vectors with different widths. Like, wire[2:0] a; reg[7:0] b;  
* Values : 0(Logical zero/false), 1(Logical one/true), X(Unknown Logic Value), Z(High Impedance).

Integers, Arrays, Memories, Parameters, Strings are few other data types.

### Concepts To Get Started 

* Module Instantiation : Process of connecting one module to another.   
Its subparts are Positional Mapping and Nomenclature Based Mapping.
```
ex 1 : module pos_map(q,clk,rst)
       output[1:0] q;
       input clk, rst;
       tflipflop lab0(q[0], clk, rst);
       tflipflop lab1(q[1], clk, rst);
       end
       
ex 2 : module nom_map(q,clk,rst)
       output[1:0] q;
       input clk, rst;
       tflipflop lab0(.q(q[0]), .clk(clk), .rst(rst));
       tflipflop lab1(.q(q[0]), .clk(clk), .rst(rst));
       end
```

* Comments : // for single line comment and /* ... */ multiple comment lines. 

* $display vs $monitor : $dispay is used to display immediate value of variables. It gets executed in an active region. $monitor gets executed whenever the value of the given variable changes in it. It gets executed in the postponed region. Monitor is required only once to be written.

### Regular Codes

* ![Data Flow Modelling](src/DataFlowModelling.v) and ![Logic Gate Modelling](src/LogicGateModelling.v)
* ![Asynchronous and Synchronous D-FlipFlop](src/AsyncAndSyncDFlipFlop.v)
* ![Four Bit Counter](src/FourBitCounter.v)
* ![Decoder 3x8](src/Decoder3x8.v)
* ![Encoder 4x2](src/Encoder4x2.v)
* ![DeMux 1x4](src/DeMux1x4.v)
* ![Mux 2x1](src/Mux2x1.v)
* ![SR Flip Flop](src/SRFlipFlop.v)
* ![JK Flip Flop](src/JKFlipFlop.v)
* ![T Flip Flop](src/TFlipFlop.v)
* ![D Flip Flop](src/DFlipFlop.v)

#### Code For Concepts

* ![Blocking Statements](src/Blocking.v) and ![Non-Blocking Statements](src/NonBlocking.v)
* ![Seven Segment Display](src/SevenSegment.v)
* ![Mealy '000' Sequence Machine](src/Mealy000Sequence.v) and ![Mealy '1001' Sequence Machine](src/Mealy1001Sequence.v)
* ![Moore '000' Sequence Machine](src/Moore000Sequence.v)
* ![Traffic Lights - Two Lights/4-Point Crossing](src/TrafficLightsFourWay.v)

### Case-Study

* ![Biometric Authorization : Authorization happens only when hashed value is matched for particular input](src/BiometricsImplement.v)

### DIY Codes

* Half Subtractor, Full Subtractor, Half Adder, Full Adder : Using DataFlow, LogicGate Modelling, case statements.
* Master-Slave JK Flip-Flop : Truth table for master and slave latch both.


