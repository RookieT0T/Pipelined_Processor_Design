# **Pipelined_Processor_Design**
This is a 16-bit pipelined processor built upon the single-cycle processor implemented in another repository. i.e. it roughly executes one instruction per clock cycle when the pipeline is full. It has five stages. i.e. instruction fetch stage, decode stage, execute stage, memory stage, and write back stage. There are 4 intermediate registers between these 5 stages, which effectively split the critical path of the single-cycle processor. Compared with the single-cycle processor, we could run the processor at a higher clock frequency and thus we acquire the higher performance.

## 4 Intermediate pipeline registers ##
IF/ID, ID/EX, EX/MEM, MEM/WB

## Data Hazard & Control Hazard
Data hazard is solved by data forwardings including RF Bypassing, MEM-to-MEM, MEM-to-EX, and EX-to-EX.

Control hazard is solved by Predict-Not-Taken strategy, flush the incorrectly fetched instruction, and insert a stall (NOP).

## High-level Processor Block Diagram

