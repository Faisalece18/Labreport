

## Code:

```matlab
1. clc
2. x = input('Enter the elements of function x within [ ] braket\n'); 
3. L = length(x); 
4. h = input('Enter the elements of function h within [ ] braket\n'); 
5. M = length(h); 
6. 
7. N = L + M -1; 
8. 
9. for i=1:N 
10. y(i)=0; 
11. for j=1:L 
12. if ((i-j+1)>0 && (i-j)<4)
13. y(i)=y(i)+x(j)*h(i-j+1); 
14. disp(y(i)); 
15. end
16. end
17. end
18. subplot(3,1,1); 
19. stem(x); 
20. title('Input Signal x(n)'); 
21. subplot(3,1,2); 
22. stem(h); 
23. title('Impulse Response h(n)'); 
24. subplot(3,1,3); 
25. stem(y); 
26. title('Convolution Result y(n)'); 


```
