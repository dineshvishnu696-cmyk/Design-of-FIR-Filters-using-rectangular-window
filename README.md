# Design-of-FIR-Filters-using-rectangular-window
#          DESIGN OF LOW PASS FIR DIGITAL FILTER 

# AIM: 
          
  To generate design of low pass FIR digital filter using SCILAB 

# APPARATUS REQUIRED: 

  PC Installed with SCILAB 

# PROGRAM 


# OUTPUT
# Design-of-FIR-Filters-using-rectangular-window
# DESIGN OF LOW PASS FIR DIGITAL FILTER 

# AIM: 
          
  To generate design of low pass FIR digital filter using SCILAB 

# APPARATUS REQUIRED: 

  PC Installed with SCILAB 

# PROGRAM 
```
clc ; 
close ; 
M=input('Enter the Odd Filter Length ='); 
Wc=input('Enter the Digital Cut off frequency ='); 
alpha= (M -1)/2 // Center Value 
for n = 1:M 
 
if (n ==alpha+1) 
 
hd(n) = Wc/ %pi ; 
else 
hd(n) = sin(Wc *((n -1)-alpha)) /(((n -1)-alpha)*%pi); 
 
end 
end 
 
 
// Rectangular Window 
22 
 
for n = 1:M 
W(n) = 1; 
end 
 
 
 
//Windowing filter coefficients 
h = hd.*W; 
disp(h,'Filter Coefficients are') 
 
 
 
[hzm,fr]= frmag (h,256) ; 
subplot(2 ,1 ,1) 
plot(2*fr, hzm) 
 
xlabel( ' Normalized Digital Frequency w'); 
ylabel( 'Magnitude '); 
title( ' Frequency Response of  FIR LPF using Rectangular Window ') 
 
 
 
hzm_dB = 20* log10 (hzm); 
subplot (2 ,1 ,2); 
plot(2*fr , hzm_dB); 
 
xlabel( ' Normalized Digital Frequency W' ); 
ylabel( 'Magnitude in dB'); 
title('Frequency Response of FIR LPF using Rectangular Window'); 

```

# OUTPUT

<img width="1920" height="1080" alt="Screenshot (149)" src="https://github.com/user-attachments/assets/47d8af98-215a-4e71-a04f-ecba82232a6b" />

<img width="1920" height="1080" alt="Screenshot (150)" src="https://github.com/user-attachments/assets/f2ba7452-42ef-468d-a304-812a960e6015" />

# RESULT:
DESIGN OF LOW PASS FIR DIGITAL FILTER using SCILAB is executed successfully.

# RESULT
