# SSB

EXP NO: 3	SSB-SC-AM MODULATION using SCILAB

AIM:

To write a program to perform SSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

Note: Keep all the switch faults in off position


Algorithm
1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the message signal.
•	Amplitude: Maximum amplitude of the message signal.
2.	Generate Signals:
•	Message Signal: The baseband signal that will be modulated.
•	Carrier Signal: A high-frequency signal used for modulation.
•	Analytic Signal: Constructed using the Hilbert transform to get the in-phase and quadrature components.
3.	SSBSC Modulation:
•	Modulated Signal: Create the SSBSC signal using the in-phase and quadrature components, modulated by the carrier.
4.	SSBSC Demodulation:
•	Mixing: Multiply the SSBSC signal with the carrier to retrieve the message signal.
•	Low-pass Filtering: Apply a low-pass filter to remove high-frequency components and recover the original message signal.
5.	Visualization:
•	Plot the message signal, carrier signal, SSBSC modulated signal, and the recovered signal after demodulation.


PROCEDURE

•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
 
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform

Model Waveform

<img width="704" height="178" alt="image" src="https://github.com/user-attachments/assets/32ee29b3-0d95-4192-9762-972d50c05c90" />
<img width="706" height="167" alt="image" src="https://github.com/user-attachments/assets/bff0d8fd-d679-444e-af37-0b34585853c1" />

Program

Am=5.4;

Ac=10.8;

fm=444;

fc=4440;

fs=44400;

t=0:1/fs:2/fm;

m1=Am*cos(2*3.14*fm*t);

m2=Am*sin(2*3.14*fm*t);

subplot(4,1,1);

plot(t,m1);

c1=Am*cos(2*3.14*fc*t);

c2=Am*sin(2*3.14*fc*t);

subplot(4,1,2);

plot(t,c1);

s1=c1.*m1;

s2=c2.*m2;

slsb=s1+s2;

subplot(4,1,3);

plot(t,slsb);

susb=s1-s2;

subplot(4,1,4);

plot(t,susb);

OUTPUT WAVEFORM


<img width="1506" height="957" alt="Screenshot 2025-09-01 221207" src="https://github.com/user-attachments/assets/a3b84484-5602-42e3-81bc-207ed6cf155d" />

TABULATION


![WhatsApp Image 2025-09-01 at 22 13 32_7a0fe6b6](https://github.com/user-attachments/assets/25ef89ae-c98b-49fb-bf2b-384f5b6325df)









RESULT:

Thus, the SSB-SC-AM Modulation and Demodulation is experimentally done and the output is verified.





