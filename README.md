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
```
clc; % clear screen
clear all; % clear screen
close all; % close all figure windows
wc1=input('enter the value of cut off frequency1' ); 
wc2=input('enter the value of cut off frequency2' );
N=input('enter the value of filter'); 
alpha=(N-1)/2; 
eps=0.001; 
%Band Stop Filter Coefficient
n=0:1:N-1; 
hd=(sin(wc1*(n-alpha+eps))+sin(pi*(n-alpha+eps))-sin(wc2*(n-alpha+eps)))./(pi*(n-alpha+eps))
% Blackman Window Sequence 
n=0:1:N-1; 
wh=0.42-0.5*cos((2*pi*n)/(N-1))+0.08*cos(4*pi*n/(N-1)) 
hn=hd.*wh 
% Plot the Band Stop Filter with Blackman Window Technique
w=0:0.01:pi; 
h=freqz(hn,1,w);   
plot(w/pi,abs(h),'ms');
```

## OUTPUT:

![WhatsApp Image 2025-11-28 at 11 24 41 PM](https://github.com/user-attachments/assets/6bc288bd-7b86-474c-83df-af3503f4d21a)



## RESULT:
![WhatsApp Image 2025-11-28 at 11 25 56 PM](https://github.com/user-attachments/assets/70a494ab-c222-435e-a5a1-5cf7b8c61c6f)

