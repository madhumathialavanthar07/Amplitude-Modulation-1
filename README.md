# Amplitude-Modulation

EXP NO: 1	GENERATION AND DETECTION OF AM

AIM:

To generate and detect the amplitude modulation and demodulation u s i n g S C I L A B and to calculate modulation index of AM.

EQUIPMENTS REQUIRED:

•	Computer with i3 Processor

•	SCI LAB

THEORY:

Modulation can be defined as the process by which the characteristics of carrier wave are varied in accordance with the modulating wave (signal). Modulation is performed in a transmitter by a circuit called a modulator.
Need for modulation is as follows:
•	Avoid mixing of signals
•	Reduction in antenna height
•	long distance communication
•	Multiplexing
•	Improve the quality of reception
•	Ease of radiation.
Amplitude Modulation is the process of changing the amplitude of a relatively high frequency carrier signal in proportion with the instantaneous value of the modulating signal. The output waveform contains all the frequencies that make up the AM signal and is used to transport the information through the system. Therefore the shape of the modulated wave is called the AM envelope. With no modulating signal the output waveform is simply the carrier signal. Coefficient of modulation is a term used to describe the amount of amplitude change present in an AM waveform. There are three degrees of modulation available based on value of modulation index.
1)	Under modulation :	m<1, Em < Ec
2)	Critical modulation: m-1, Em = Ec
3)	Over modulation:	m>1, Em > Ec



Note: Keep all the switch faults in off position

Algorithm:
1.	Define Parameters
First, define the parameters for your signals:
•	Carrier frequency (fc)
•	Modulating signal frequency (fm)
•	Sampling frequency (Fs)
•	Duration of the signal (T)


2.	Create a time vector based on the sampling frequency and duration.
 
3.	Create Modulating Signal
Define the modulating signal (message signal).

4.	Create Carrier Signal
Define the carrier signal.


5.	Perform Amplitude Modulation
Multiply the carrier signal by the modulating signal plus 1 (to ensure the modulation depth).


6.	Plot the Signals
Visualize the modulating, carrier, and modulated signals.


7.	Demodulate the AM Signal
To demodulate, you can use envelope detection. One way is to rectify the signal and then apply a low-pass filter.

8.	Plot the Demodulated Signal
Visualize the demodulated signal.


9.	Compare Signals
Compare the original modulating signal with the demodulated signal. PROCEDURE
•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform

Program:
clc; clear; close; Ac=13; Am=6.5; Fc=4990; Fm=499; Fs=40000; t=0:1/Fs:2/Fm; E1=Amsin(2%piFmt); subplot(4,1,1); plot(t,E1); xlabel("Time(s"); ylabel("Amplitude"); title("Message Signal"); E2=Acsin(2%piFct); subplot(4,1,2); plot(t,E2); xlabel("Time(s"); ylabel("Amplitude"); title("Carrier Signal"); E3=(Ac+Amsin(2%piFmt)).sin(2%piFct); subplot(4,1,3); plot(t,E3); xlabel("Time(s"); ylabel("Amplitude"); title("AM Signal"); demodulated_signal=abs(hilbert(E3))-Ac; subplot(4,1,4); plot(t,demodulated_signal); xlabel("Time(s"); ylabel("Amplitude"); title("Demodulated Signal"); xgrid();

Output Waveform:
![WhatsApp Image 2025-10-13 at 21 39 04_48c9d3f8](https://github.com/user-attachments/assets/ed5e01cd-5419-466e-89d0-833dd876b96b)

TABULATION:

![WhatsApp Image 2025-10-28 at 23 07 02_fd0519f6](https://github.com/user-attachments/assets/01c6a68f-ace5-4c33-810a-af932ef86b61)

Calculation:
1.	ma (Theory) = am/ac = 0.5
2.	ma(Practical) = (Emax-Emin)/(Emax+Emin) =0.2540

MODEL GRAPH:
 <img width="919" height="1290" alt="image" src="https://github.com/user-attachments/assets/55326c5b-7dd5-4873-aaf6-d219bb7c4420" />

 
RESULT:
Thus the amplitude modulation and demodulation is experimentally done and the output is verified.
