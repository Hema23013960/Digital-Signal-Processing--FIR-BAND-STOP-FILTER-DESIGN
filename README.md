# Digital-Signal-Processing--FIR-BAND-STOP-FILTER-DESIGN
## AIM:
To generate design of Band Stop FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Band Stop filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
clc; % clear screen<br>
clear all; % clear screen<br>
close all; % close all figure windows<br>
wc1=input('enter the value of cut off frequency wc1'); <br>
wc2=input('enter the value of cut off frequency wc2'); <br>
N=input('enter the value of filter'); <br>
alpha=(N-1)/2; <br>
eps=0.001; <br>
%Band Pass Filter Coefficient<br>
n=0:1:N-1; <br>
hd=(sin(wc1*(n-alpha+eps))-sin(wc2*(n-alpha+eps)))./((n-alpha+eps)*pi)<br>
%Bartlett Window Sequence <br>
n=0:1:N-1; <br>
wh = 1 - abs(n - alpha) / alpha;<br>
hn=hd.*wh<br>
% Plot the Band Pass Filter with Hanning Window Technique<br>
w=0:0.01:pi; <br>
h=freqz(hn,1,w);<br>
plot(w/pi,abs(h),'blue');<br>


## OUTPUT:
![WhatsApp Image 2025-11-23 at 15 58 52_d822250a](https://github.com/user-attachments/assets/6f8cec43-c5f7-482b-8af2-526e2906cc7d)


## RESULT:
![WhatsApp Image 2025-11-28 at 22 31 29_3cb3a41b](https://github.com/user-attachments/assets/32fa9f41-daee-48b8-bc2c-dfb6210bce80)

