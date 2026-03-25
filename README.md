# Digital-Signal-Processing--FIR-LOW-PASS-FILTER-DESIGN
## AIM:
To generate design of low pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Low Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```
clc; % clear screen 
clear all; % clear screen 
close all; % close all figure windows 
wc=input('enter the value of cut off frequency');  
N=input('enter the value of filter');  
alpha=(N-1)/2;  
eps=0.001;  
%High Pass Filter Coefficient 
n=0:1:N-1;  
hd=(sin(pi*(n-alpha+eps))-sin((n-alpha+eps)*wc))./(pi*(n-alpha+eps)) 
%Hamming Window Sequence  
n=0:1:N-1;  
wh=0.54-0.46*cos((2*pi*n)/(N-1)) 
hn=hd.*wh
% Plot the high Pass Filter with Hanning Window Technique 
w=0:0.01:pi;  
h=freqz(hn,1,w);  
plot(w/pi,abs(h),'ms');
```
## OUTPUT:
![WhatsApp Image 2026-03-25 at 11 21 01 PM](https://github.com/user-attachments/assets/cfd29cd3-5f94-4cbb-9582-a0f197aa0b2d)

## RESULT:
![WhatsApp Image 2026-03-25 at 11 23 03 PM](https://github.com/user-attachments/assets/17bd7f1e-928f-41e3-bba0-f5474c6ed144)
