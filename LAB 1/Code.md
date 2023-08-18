

## Code:

```matlab
Code 1: Unit step, unit impulse and unit ramp

1. clc; 
2. clear all; 
3. close all; 
4. t=-5:0.001:5; 
5. step1= t>= 0; 
6. step2= t==0; 
7. 8. step3= (t>=0).*t; 
8. subplot(3,1,1); 
9. plot(t,step1); 
10. xlabel('Time'); 
11. ylabel('Amplitude'); 
12. title('Unit step'); 
13. 15. ylim([-0.1, 1.1]); 
14. subplot(3,1,2); 
15. plot(t,step2); 
16. xlabel('Time'); 
17. ylabel('Amplitude'); 
18. title('Unit Impluse'); 
19. 22. ylim([-0.1, 1.1]); 
20. subplot(3,1,3); 
21. plot(t,step3); 
22. xlabel('Time'); 
23. ylabel('Amplitude'); 
24. title('Unit ramp'); 
25. ylim([-0.5, 5.5]); 

Code 2: Discrete signal -

1. clc; 
2. clear all; 
3. close all; 
4. x=[2, 0, -2, 3, 1, 4, 6]; 
5. n=[1 2 4 5 6 8 3]; 
6. stem(n,x); 
7. xlabel('n'); 
8. ylabel('x'); 
9. xlim([0, 9]); 
10. ylim([-3, 7]); 

Code 3: Two different signals, their addition and subtraction

1. clc; 
2. clear all; 
3. close all; 
4. t=-10:1:20; 
5. step1= t>=0 & t<=10; 
6. step2= t>=5 & t<=15; 
7. subplot(4,1,1); 
8. stem(t,step1); 
9. xlabel('Time'); 
10. ylabel('Amplitude'); 
11. 13. title('Signal 1'); 
12. subplot(4,1,2); 
13. stem(t,step2); 
14. xlabel('Time'); 
15. ylabel('Amplitude'); 
16. title('Signal 2'); 
17. step3 = step1+step2 
18. subplot(4,1,3); 
19. stem(t,step3); 
20. xlabel('Time'); 
21. ylabel('Amplitude'); 
26. title('Addition'); 
22. step4 = step1-step2 
23. subplot(4,1,4); 
24. stem(t,step4); 
25. xlabel('Time'); 
26. ylabel('Amplitude'); 
27. title('Subtraction'); 
Code 4: Presentation of two signals

1. clc; 
2. clear all; 
3. close all; 
4. 
5. t=0:1:7; 
6. u = [ones(1,1).*1 ones(1,2).*2 ones(1,1).*4 ones(1,1).*4 ones(1,2).*2
ones(1,1)]; 
7. subplot(2,1,1); 
8. plot(t,u); 
9. xlabel('Time'); 
10. ylabel('Amplitude'); 
11. title('Signal 1'); 
12. xlim=([0, 8]); 13. ylim([1, 5]); 
14. 
15. t=0:1:6; 
16. u1 = [zeros(1,1) ones(1,5) zeros(1,1)]; 
17. subplot(2,1,2); 
18. plot(t,u1); 
19. xlabel('Time'); 
20. ylabel('Amplitude'); 
21. title('Signal 2'); 
22. xlim=([-0, 7]); 
23. ylim([0, 1.1]); 

```
