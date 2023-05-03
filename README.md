Download Link: https://assignmentchef.com/product/solved-cs224-sp-lab-5
<br>
<strong>Implementing the MIPS Processor with Pipelined Microarchitecture</strong>




<strong>MUST (PART 1)</strong>

<ul>

 <li>Answer the questions given in Part 1)a-f in a PDF report. Give your test codes in this report as well. If you need to explain your modifications in the processor, you can do in the report as well.</li>

 <li>You will modify the given System Verilog Skeleton code to reflect the changes asked in Part 1-f. Put this in a TXT file for submission to MOSS testing.</li>

 <li>You will create programs to test your processor as outlined in Part 1-e. Submit these assembly instructions both in yout PDF and TXT files. This will be used to test your Processor with the modifications you made. Submit this as part of the code. The best way to put assembly codes in your submission would be to put the HEX instructions and after each line you can add a comment to indicate the corresponding assembly instruction.</li>

</ul>




<strong>OPTIONAL (PART 2)</strong>

<ul>

 <li>You may simulate/synthesize and test it on Vivado if your modified processor properly executes all the instructions.</li>

 <li>Testbench</li>

</ul>




<strong>Purpose</strong>: In this lab you will implement and test a pipelined MIPS processor using the digital design engineering tools (System Verilog HDL, Xilinx Vivado).  To do this, you will need to add pipeline registers, forwarding MUXes, a hazard unit, etc. to your datapath, and of course make the control pipelined as well.  You will be provided a skeleton System Verilog code for the Pipelined MIPS processor and fill the necessary parts to make it work.




<strong>Summary </strong>

<strong>Part 1</strong> (100 points): Design Report: Pipeline hazards evaluation and preparing test modules in MIPS.

<strong>Part 2</strong> (Optional): Implementation and simulation of the MIPS-lite pipelined processor.

You will <strong>upload your lab work</strong> as <strong>one PDF</strong> and <strong>one TXT</strong> file in two separate submissions to Unilica Assignment. Code submissions will be used for similarity testing by MOSS.  Please see the related section below for further instructions on MOSS submission.

<strong>If we suspect that there is cheating, we will send the work with the names of the students to the university disciplinary committee.</strong>

<strong> </strong>

<strong>Part 1. Design Report (100 points)</strong>




At the end of this lab, you will have implemented the pipelined MIPS architecture that can be seen in the file that is provided as <strong><em>PipelineDatapath.PNG</em></strong> (Notice that there is no early branch prediction in this pipeline. Hence, the branch resolution is done in the Decode stage.). Note also that there is no jump instruction implemented as well. Your Design Report should contain the following items along with code submission to Unilica:




<ol>

 <li>a) Cover page, with university name, department name, and course name and number at the top, “Design Report”, Lab # (e.g. 5), Section #, and your name and ID# in the middle, and the date of your lab at the bottom.</li>

 <li>b) <strong>[15 points] </strong>The list of all hazards that can occur in this pipeline. For each hazard, give its type (data or control), its specific name (“compute-use” “load-use”, “load-store”, “branch” etc.), the pipeline stages that are affected.</li>

 <li>c) <strong>[15 points] </strong>For each hazard, give the solution (forwarding, stalling, flushing, combination of these), and explanation of what, when, how.</li>

 <li>d) <strong>[15 points] </strong>The logic equations for each signal output by the hazard unit, as a function of the input signals that come to the hazard unit. This hazard unit should handle all the data and control hazards that can occur in your pipeline (listed in b) so that your pipelined processor computes correctly.</li>

 <li>e) <strong>[20 points] </strong>Write small test programs, in MIPS assembly, that will show whether the pipelined processor is working or not. Each of your test programs should be designed to catch problems, if there are any, in the execution of MIPS instructions in your pipelined machine. Write:</li>

</ol>

<ul>

 <li>A test program with no hazards (to verify that there are no problems with the connections in your pipeline etc.)</li>

 <li>A test program that has one type of hazard, and another, and another…</li>

</ul>

In the end, have at least 4 test programs (testing at least 3 hazards) with their machine code (in hex).

<em>You can use the student-written assembler tool available online to help you quickly implement your test programs<a href="#_ftn1" name="_ftnref1"><strong>[1]</strong></a>.  Remember that the goal of testing is to verify that all the instructions are fully working, <u>and</u> that all the instructions are working even in the presence of hazards.</em>

<ol>

 <li>f) <strong>[35 points] </strong>You are given a skeleton System Verilog code for your pipelined MIPS processor in the file <strong><em>txt</em></strong>. The places in the code that needs to be modified are shown with comment blocks above them. Fill them to implement Pipelined Processor. You don’t need to follow the skeleton code point by point. If you think your design is better, you are welcome to try it in your code, as long as your version of the code works, too.</li>

</ol>

<strong>Part 2:  Implementation and Simulation (Optional)</strong>

<ol>

 <li>a) Now make a System Verilog testbench file and using Xilinx Vivado, simulate your Pipeline Processor by executing the test programs you wrote at Prelim e). Implement a new top module in order to see memwrite, regwrite, writedata, pc, instruction and resultw signals. Study the results given in the simulation window. Find each instruction, and understand its values. Do this step for each of the test programs you wrote.</li>

 <li>b) When you have integrated all the System Verilog modules together and your whole pipelined MIPS is working in simulation with the test programs you wrote, call<u> the TA and show it for grade</u>. To get full points from this part, you must know and understand everything about what you have done.</li>

</ol>





