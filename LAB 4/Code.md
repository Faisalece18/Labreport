

## Code:
### Identifying Delays:
```matlab
1. clc
2. clear all
3. close all
4. fs=1000
5. t = 0:0.001:1; 
6. frequency = 10; 
7. dutyCycle = 50; 
8. delay = 0.15; 
9.
10. signal = square(2*pi*frequency*t, dutyCycle);
11. subplot(3,1,1)
12. plot(signal)
13. title('Given Square Wave')
14. signalWithDelay = [zeros(1, round(delay*fs)), signal(1:end-round(delay*fs))];
15. subplot(3,1,2)
16. title('Delayed Version of the Square Wave')
17. plot(signalWithDelay)
18. [correlation, lag] = xcorr(signal, signalWithDelay);
19. subplot(3,1,3)
20. plot(lag, correlation)
21. title('Auto Correlation')


```
###  Periodicity:
```matlab
1. clc
2. clear all
3. close all
4.
5. fs = 1000; 
6. t = 0:1/fs:1; 
7. f = 10; 
8. x = sin(2*pi*f*t);
9.
10. shift_amount = 0.25; 
11. shifted_x = [zeros(1, round(shift_amount*fs)), x(1:end-round(shift_amount*fs))];
12.
13. autocorr_x = xcorr(x);
14. autocorr_shifted_x = xcorr(shifted_x);
15.
16. lags = -length(x)+1:length(x)-1;
17. figure;
18. subplot(4, 1, 1);
19. plot(x);
20. title('Main Signal');
21. subplot(4, 1, 2);
22. plot(shifted_x);
23. title('Shifted Signal');
24. subplot(4, 1, 3);
25. plot(lags, autocorr_x);
26. title('Autocorrelation of Original Signal');
27.
28. subplot(4, 1, 4);
29. plot(lags, autocorr_shifted_x);
30. title('Autocorrelation of Time-Shifted Signal');
31. if autocorr_x(length(x)+1) > 0.9 * max(autocorr_x)
32. disp('Signal exhibits periodicity with a time-shifted version.');
33. else
34. disp('Signal does not exhibit clear periodicity with a time-shifted version.');
35. End

```
