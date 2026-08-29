# 5-Stage-Instruction-Pipelined-RISC-Processor
In case of pipelined implementation what we do is that we divide our instruction into multiple stages and in case of 5 stage pipelined implementation we will offcourse divide the instruction into 5 different stages. Five different stages are given as:

Instruction Fetch
Instruction Decode
Instruction Execution
Memory Read/Write
Write Back
This pipelined implementation of processor supports six basic instructions:

R-Type
I-Type
S-Type
B-Type
J-Type
U-Type
# Implementation and Procedure
5 Stage pipeline requires a series of registers between the complete datapath, these registers will be responsible for tracking of instruction or different partss of instructions required by different modules. The instructions needs to be propogated into all five stages for the instruction to be executed correctly and with the help of these registers the corresponding instructions propogate or different parts of instructions accordingly. The datapath followed is mentioned below and is the extened version of same implemented single cycle datapath.

# Discussions
1. Fetch Cycle Datapath

The Fetch cycle is the first stage of instruction execution process. The main goal of the fetch cycle is to retrieve the next instruction from memory so that it can be decoded and executed by the processor.

2. Decode Cycle Datapath

The decode cycle in a is the second stage of instruction execution. The main objective of this stage is to interpret the fetched instruction and prepare the necessary inputs (registers, control signals) for subsequent stages.

3. Execution Cycle Datapath

The Execution cycle is the third stage of instruction execution process. Its main role is to perform the arithmetic or logical operation dictated by the instruction, calculate memory addresses for load/store operations, or determine the outcome of a branch.

4. Memory Read/Write Cycle Datapath

The Memory Read or Write Cycle is the fourth stage of instruction execution process. This stage is responsible for interacting with data memory during load or store instructions. If the instruction is not a memory operation, this stage is skipped, and the processor moves to the writeback stage.

5. Write Back Cycle Datapath

The Writeback cycle is the fifth and final stage of instruction execution process. The main purpose of this stage is to write the result of an instruction (whether it be from an arithmetic operation or a memory load) back to the destination register.

Note: Hazard Unit

Hazard units in a pipeline processor are responsible for detecting and resolving hazards that can occur when executing instructions in a pipelined
architecture. Hazards can cause incorrect program execution or reduce performance by stalling the pipeline. There are three primary types of hazards: data hazards, control hazards, and structural hazards. In a 32-bit RISC-V 5-stage pipeline, hazard detection and forwarding units are critical components that help manage these hazards.

Structural Hazard

Hardware does not support the execution of instruction in same clock cycle.
Without having Two memories RISC-V pipelining architecture will have structural hazard.
Data Hazard

Data to be executed is not available.
May occur when pipeline is stalled.
Solve by using forwarding or bypassing technique.
