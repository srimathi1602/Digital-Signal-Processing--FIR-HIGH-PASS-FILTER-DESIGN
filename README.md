# Digital-Signal-Processing--FIR-HIGH-PASS-FILTER-DESIGN
## AIM:
To generate design of High pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the hIGH Pass filter Coefficient.

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
%Hanning Window Sequence 
n=0:1:N-1; 
wh=0.5-0.5*cos((2*pi*n)/(N-1)) 
hn=hd.*wh 
% Plot the High Pass Filter with Hanning Window Technique
w=0:0.01:pi; 
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');
```

## OUTPUT:

<img width="694" height="619" alt="Screenshot 2025-11-12 102944" src="https://github.com/user-attachments/assets/5fd7e6b5-ca0c-4f90-984f-539b5a6716b6" />


## RESULT:

![WhatsApp Image 2025-11-24 at 22 49 20_77768806](https://github.com/user-attachments/assets/8c05bbfc-ca99-462f-9917-a1878ee7f3f9)

