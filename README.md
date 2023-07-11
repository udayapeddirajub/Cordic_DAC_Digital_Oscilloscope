# Cordic_DAC_Digital_Oscilloscope
The sine and cosine waveform generator design consists of the following components: 
1)  CORDIC Algorithm: The CORDIC algorithm is used to compute the sine function. It uses a series of rotations 
to approximate the angle of a vector. The algorithm can be implemented using a look-up table or a pipelined 
architecture. I have designed a three-stage pipelined and a look-up table architecture. 
2)  Frequency Input: The desired frequency of the sine waveform is input using slide switches on the BASYS3 
board. The frequency is used to compute the angle of the vector for the CORDIC algorithm. 
3)  Sine Function: Once the angle is computed from the CORDIC algorithm and the desired frequency input, the 
sine function is used to generate the waveform.  
4)  Pmod DAC2: The Pmod DAC2 is used to convert the digital waveform to an analogue signal and display it on 
a digital oscilloscope. 
5)  The CORDIC algorithm was implemented using a pipelined architecture in Verilog. The Verilog code was 
synthesized using Xilinx Vivado and implemented on the BASYS3 board. The input frequency was read using 
the BASYS3 board's slide switches and converted to radians for the CORDIC algorithm. The sine function was 
computed using a look-up table, which was precomputed using MATLAB and stored in ROM on the FPGA. 
The design was tested with all the timing constraints and also the post-timing analysis was shown in an analogue 
view. The input frequency is an 8-bit number which is used to translate into the phase for the CORDIC sine wave 
generator, the maximum frequency signal that is generated is 268KHz and is obtained when slide switches are in 
maximum range and the frequency is varied with a change in slide switches. 
