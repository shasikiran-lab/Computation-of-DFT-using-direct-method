# EXPT 1: Computation-of-DFT-using-direct-method

## AIM
To perform and verify DFT using direct method by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 

// DISCRETE FOURIER TRANSFORM 

DIRECT METHOD:

clc;

clear;

clf;

xn = [1,2,3,4,4,3,2,1];

N = length(xn);

n = 0:N-1;

j = %i;

Xk = zeros(1, N);

// Direct DFT calculation
for k = 0:N-1

    for r = 0:N-1
        Xk(k+1) = Xk(k+1) + ...
            xn(r+1)*exp(-j*2*%pi*k*r/N);
    end
end

disp("DFT output:");

disp(Xk);

K = 0:N-1;

magnitude = abs(Xk);

phase = atan(imag(Xk), real(Xk));

subplot(3,1,1);

plot2d3(n, xn);

xtitle("Input Sequence", "n", "x(n)");

subplot(3,1,2);

plot2d3(K, magnitude);

xtitle("Magnitude Spectrum", "k", "|X(k)|");

subplot(3,1,3);

plot2d3(K, phase);

xtitle("Phase Spectrum", "k", "Phase (radians)"

### CALCULATIONS:

<img width="702" height="1280" alt="image" src="https://github.com/user-attachments/assets/6c807c09-45ce-410c-8758-13b2cb264080" />
<img width="736" height="1280" alt="image" src="https://github.com/user-attachments/assets/c1a31033-dc76-4ade-9f2a-66a9f4cd0311" />
<img width="846" height="1280" alt="image" src="https://github.com/user-attachments/assets/a2abe3d9-7bb8-4eb4-a2b6-7825cdd471ab" />
<img width="852" height="1280" alt="image" src="https://github.com/user-attachments/assets/f6f1da57-1c6e-442a-9022-067fc20ec628" />

### SAMPLE OUTPUT:

<img width="1228" height="1280" alt="image" src="https://github.com/user-attachments/assets/bbcc10fa-e3cb-4137-83af-d27a360e135b" />

## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.
