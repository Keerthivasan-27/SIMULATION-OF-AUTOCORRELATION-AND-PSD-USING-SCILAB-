# SIMULATION-OF-AUTOCORRELATION-AND-PSD-USING-SCILAB-
## AIM
Write a program for Autocorrelation and PSD of signals in SCILAB and verify Wiener-Khinchin relation.

## EQUIPMENTS NEEDED

•	Computer with i3 Processor
•	SCI LAB

## THEORY
The Wiener-Khinchin theorem states that the power spectral density of a wide sense stationary random process is the Fourier transform of the corresponding autocorrelation function.
<img width="582" height="91" alt="image" src="https://github.com/user-attachments/assets/dacf7cfd-96c5-45a6-aa31-321978d15f97" />

## ALGORITHM
1.	Load or Define the Signal: Input your time-domain signal.
2.	Compute Autocorrelation: Calculate the autocorrelation function of the signal.
3.	Compute Power Spectral Density (PSD): Estimate the PSD of the signal, either directly using a method like Welch’s periodogram or by using the Fourier transform of the autocorrelation.
4.	Plot Results: Visualize the autocorrelation function and PSD.

## PROCEDURE

•	Refer Algorithms and write code for the experiment.

•	Open SCILAB in System

•	Type your code in New Editor

•	Save the file

•	Execute the code

•	If any Error, correct it in code and execute again

•	Verify the generated waveform using Tabulation and Model Waveform

## PROGRAM
clc;
clear;

// --- Time vector and signal ---
t = 0:0.01:2*%pi;
x = sin(2*t);

// --- Plot original signal ---
subplot(3,2,1);
plot(t, x);
title("Original Signal x(t)");

// --- Autocorrelation ---
au = xcorr(x, x);
subplot(3,2,2);
plot(au);
title("Autocorrelation of x");

// --- FFT of autocorrelation ---
v = fft(au);
subplot(3,2,3);
plot(abs(v));
title("FFT of Autocorrelation");

// --- FFT of original signal ---
fw = fft(x);
subplot(3,2,4);
plot(abs(fw));
title("FFT of x(t)");

// --- Power Spectrum of original signal ---
fw2 = abs(fw).^2;
subplot(3,2,5);
plot(fw2);
title("Power Spectrum of x(t)");

## OUTPUT
![WhatsApp Image 2025-11-19 at 20 04 10_d2db38a5](https://github.com/user-attachments/assets/28259ef2-124d-4fc3-9c51-c22e89880e67)


## RESULT`
Thus the auto correlation and PSD are executed and the output is verified 



