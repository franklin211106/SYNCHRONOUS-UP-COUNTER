## NAME:FRANKLIN.F
## REF.NO:24900641

# EXPERIMENT 7: IMPLEMENTATION OF SYNCHRONOUS-UP-COUNTER

# AIM:

To implement 4 bit synchronous up counter and validate functionality.

# SOFTWARE REQUIRED:

Quartus prime

# THEORY

# 4 bit synchronous UP Counter

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

# Procedure

1.Launch Quartus on your computer and create a new project: Go to File → New Project Wizard. Specify the project name, directory, and top-level entity name. Create the synchronous up counter and implement the synchronous up counter by writing VHDL/Verilog code. Go to File → New → Select Verilog File. Compile the Project Click on Processing → Start Compilation. Fix any syntax or schematic errors if present. Simulate the Circuit: Go to Tools → University Program VWF. Define the inputs for CLK,out,rstn in the waveform editor. Run the simulation and observe the waveforms.

# PROGRAM
 
![WhatsApp Image 2024-12-20 at 22 58 39_abd0abd2](https://github.com/user-attachments/assets/56ceb8d3-b3e8-414f-b42d-26b9ed3a65df)



# RTL LOGIC UP COUNTER
![WhatsApp Image 2024-12-20 at 22 58 32_b757158a](https://github.com/user-attachments/assets/491e6175-bfe2-4965-a294-6c4775527761)


# output waveform
![WhatsApp Image 2024-12-20 at 22 57 21_aa337027](https://github.com/user-attachments/assets/361acf96-1230-4a30-bdea-57f158a41023)

# TRUTH TABLE
![WhatsApp Image 2024-12-20 at 22 58 06_7c82311d](https://github.com/user-attachments/assets/901ecd1f-5f7a-4cc6-88cc-5c6988a7bae9)


# RESULTS
Thus,implemented 4 bit synchronous up counter and validate functionality.
