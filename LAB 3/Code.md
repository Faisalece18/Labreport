

## Code:
### (Auto-correlation) 
```matlab
1. clc
2. clear all
3. %x = input('Enter x: ')
4. x=[1 2 3 4];
5. y = fliplr(x);
6. N1 = length(x);
7. N2 = length(y);
8. n = N1+N2-1
9. 
10. R_man= zeros(1,n);
11. 
12. for i=0: n
13. for j=0: n
14. if((i-j+1)>0 && (i-j+1)<=N2 && (j+1)<=N1)
15. R_man(i+1)=R_man(i+1)+x(j+1)*y(i-j+1);
16. end
17. end
18. end
19. 
20. R_man
21. R_fun = xcorr(x,x)
22. 
23. subplot(3,1,1); stem(x); title('');
24. subplot(3,1,2); stem(R_man); title('R_{manual}');
25. subplot(3,1,3); stem(R_fun); title('R_{function}');

```
###  (Cross-correlation) 
```matlab
1. clc
2. clear all
3. x = input('Enter x: ')
4. y = input('Enter y: ')
5. R_fun = xcorr(x,y);
6. y = fliplr(y);
7. N1 = length(x);
8. N2 = length(y);
9. 
10. n = N1+N2-1;
11. R_man = zeros(1,n);
12. 
13. for i=0: n
14. for j=0: n
15. if((i-j+1)>0 && (i-j+1)<=N2 && (j+1)<=N1)
16. R_man(i+1)=R_man(i+1)+x(j+1)*y(i-j+1);
17. end
18. end
19. end
20. %p=[1 2 3]
21. %p'
22. %p(1)
23. %p=fliplr(p)
24. %p(1)
25. R_man
26. R_fun
27. subplot(4,1,1); stem(x); title('X');
28. subplot(4,1,2); stem(y); title('Y');
29. subplot(4,1,3); stem(R_man); title('R_{manual}');
30. subplot(4,1,4); stem(R_fun); title('R_{function}');

```
