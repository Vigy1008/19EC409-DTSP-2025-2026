# EXP 1 : Linear and Circular Convolution

## AIM: 

 To perform Linear and Circular Convolution for two given sequence using SCILAB. 

## APPARATUS REQUIRED: 
PC installed with SCILAB. 

## PROGRAM 
```
clc; clear;

// Input sequences
x = input("Enter first sequence x: ");   
h = input("Enter second sequence h: ");  

// --- Linear Convolution ---
y_lin = conv(x, h);
disp("Linear Convolution:");
disp(y_lin);

// --- Circular Convolution ---
N = max(length(x), length(h));   
x_pad = [x, zeros(1, N - length(x))];
h_pad = [h, zeros(1, N - length(h))];

y_circ = real(ifft(fft(x_pad) .* fft(h_pad)));
disp("Circular Convolution:");
disp(y_circ);
```


## OUTPUT 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/008f271f-7edc-4e5e-9d3b-cbb8b7785f66" />


## RESULT: 
Hence Linear and Circular Convolution is verified successfully.
