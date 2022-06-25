### EX.NO : 04

### DATE : 

# <p align="center"> Correlation and Regression for Data Analysis </p>
# Aim : 

To analyse given data using  coeffificient of correlation and regression line.
![image](https://user-images.githubusercontent.com/104613195/168224136-d6b64e64-7d3d-4775-9337-c8f96fe41f2d.png)


# Software required :  

Python

# Theory:

Correlation describes the strength of an association between two variables, and is completely symmetrical, the correlation between A and B is the same as the correlation between B and A. However, if the two variables are related it means that when one changes by a certain amount the other changes on an average by a certain amount.  

If y represents the dependent variable and x the independent variable, this relationship is described as the regression of y on x. The relationship can be represented by a simple equation called the regression equation. The regression equation representing how much y changes with any given change of x can be used to construct a regression line on a scatter diagram, and in the simplest case this is assumed to be a straight line.

# Procedure :

![image](https://user-images.githubusercontent.com/104613195/168225866-ac8f6610-bdc3-4ac2-a24e-2b24ba08e189.png)

# Program:
### Developed By
### Register Number: 212220230038
### Name: PRIYADARSHINI R
```python
import numpy as np
import math
import matplotlib.pyplot as plt
x=[25,28,35,32,31,36,29,38,34,32]
y=[43,46,49,41,36,32,31,30,33,39]
Sx=0
Sy=0
Sxy=0
Sx2=0
Sy2=0
for i in range(0,10):
    Sx=Sx+x[i]
    Sy=Sy+y[i]
    Sxy=Sxy+x[i]*y[i]
    Sx2=Sx2+x[i]**2
    Sy2=Sy2+y[i]**2
N=10
r=(N*Sxy-Sx*Sy)/(math.sqrt(N*Sx2-Sx**2)*math.sqrt(N*Sy2-Sy**2))
print("The correlation coefficient is %0.3f"%r)
byx=(N*Sxy-Sx*Sy)/(N*Sx2-Sx**2)
xmean=Sx/N
ymean=Sy/N
print("The regression line Y on X is ::: Y = %0.3f %0.3f(X-%0.3f)"%(ymean,byx,xmean))
plt.scatter(x,y)
def Reg(x):
    return ymean + byx*(x-xmean)
x=np.linspace(20,40,51)
y1=Reg(x)
plt.plot(x,y1,'r')
plt.title("Fitting Regression Line")
plt.xlabel("X data")
plt.ylabel("Y data")
plt.legend(['Regression line','Data Points'])
plt.show()

```
# Output :

![out1](https://user-images.githubusercontent.com/81132849/170188272-c5c75426-175c-4561-999d-60928dd10059.png)
![out2](https://user-images.githubusercontent.com/81132849/170188305-9fef56c2-042f-4be2-a095-388ebe6604af.png)
![out3](https://user-images.githubusercontent.com/81132849/170188334-a15c77bb-7732-4898-beb9-13f17a141fb6.png)

# Results :
Thus, the Coefficient of correlation and regression line using given data was analysed.

