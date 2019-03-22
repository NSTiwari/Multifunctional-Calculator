# Multifunctional Calculator
This is a CUI application created using C programming language which works as a multi-purpose calculator. Check the document for brief description of this project.

#Code:

#include<stdio.h>
#include<conio.h>
#include<math.h>
#define pi 3.1415
int main()
  {
  int a,b,c,c1,c2,c3,c4,option,numerator,denominator,remainder;
  float x,y,z,z1,z2,z3,z4,z5;
  double d,e;
  clrscr();
  printf("\nMenu\n1.Arithmetic\n2.Logic\n3.Unit Convertors\n4.Mensuration\n");
  printf("\nEnter option\t");
  scanf("%d",&option);
  switch(option)
  {
  case 1:
  clrscr();
  printf("\nArithmetic\n\n1.Addition\n2.Subtraction\n3.Multiplication\n4.Division\n5.Modulus\n6.Logarithm");
  printf("\n7.Power\n8.Trigonometry\n\9.Factorial\n10.LCM & GCD\n");
  printf("\nEnter option\t");
  scanf("%d",&option);
  switch(option)
  {
  case 1:
  clrscr();
  printf("Enter two numbers\t");
  scanf("%d%d",&a,&b);
  c=a+b;
  printf("%d+%d=%d\t",a,b,c);
  break;
  case 2:
  clrscr();
  printf("Enter two numbers\t");
scanf("%d%d",&a,&b);
c=a-b;
printf("%d-%d=%d\t",a,b,c);
break;
case 3:
clrscr();
printf("Enter two numbers\t");
scanf("%d%d",&a,&b);
c=a*b;
printf("%dx%d=%d\t",a,b,c);
break;
case 4:
clrscr();
printf("Enter two numbers\t");
scanf("%f%f",&x,&y);
z=x/y;
printf("%0.2f/%0.2f=%0.2f\t",x,y,z);
break;
case 5:
clrscr();
printf("Enter two numbers\t");
scanf("%d%d",&a,&b);
c=a%b;
printf("%d%%%d=%d\t",a,b,c);
break;
case 6:
clrscr();
printf("Enter the number\n");
scanf("%d",&a);
d=log(a);
e=log10(a);
printf("ln(%d)=%0.3lf\n",a,d);
printf("log(%d)=%0.3lf\n",a,e);
break;
case 7:
clrscr();
printf("Enter the number and power\t");
scanf("%f%f",&x,&y);
z=pow(x,y);
printf("%0.1f to the power %0.1f is %0.3f",x,y,z);
break;
case 8:
clrscr();
printf("Enter angle in degrees\t");
scanf("%d",&a);
z=(a*pi)/180;
y=sin(z);
z1=cos(z);
z2=tan(z);
z3=1/y;
z4=1/z1;
z5=1/z2;
printf("sin(%d)=%0.3f\n",a,y);
printf("cos(%d)=%0.3f\n",a,z1);
if(a==90)
printf("tan(%d)=Not defined\n",a);
else
printf("tan(%d)=%0.3f\n",a,z2);
if(a==0)
printf("cosec(%d)=Not defined\n",a);
else
printf("cosec(%d)=%0.3f\n",a,z3);
if(a==90)
printf("sec(%d)=Not defined\n",a);
else
printf("sec(%d)=%0.3f\n",a,z4);
if(a==0)
printf("cot(%d)=Not defined\n",a);
else
printf("cot(%d)=%0.3f\n",a,z5);
break;
case 9:
clrscr();
printf("Enter the number\n");
scanf("%d",&a);
d=1;
b=1;
while(b<=a)
{
d=d*b;
b++;
}
printf("%d!=%0.1lf",a,d);
break;
case 10:
clrscr();
printf("Enter two numbers\n");
scanf("%d%d",&a,&b);
if(a>b)
{
numerator=a;
denominator=b;
}
else
{
numerator=b;
denominator=a;
}
remainder=numerator%denominator;
while(remainder!=0)
{
numerator=denominator;
denominator=remainder;
remainder=numerator%denominator;
}
c1=denominator;
c2=a*b/c1;
printf("LCM of %d and %d = %d\n",a,b,c2);
printf("GCD of %d and %d = %d\n",a,b,c1);
break;
default:
printf("Error\n");
}
break;
case 2:
clrscr();
printf("Logic\n\n");
printf("Enter two binary numbers\t");
scanf("%d%d",&a,&b);
c1=a&b;
c2=a|b;
c3=a^b;
c4=!a;
c=!b;
printf("%d AND %d = %d\n",a,b,c1);
printf("%d OR %d = %d\n",a,b,c2);
printf("%d XOR %d = %d\n",a,b,c3);
printf("%d'=%d\n",a,c4);
printf("%d'=%d\n",b,c);
break;
case 3:
clrscr();
printf("\nUnit Convertors\n\n1.Temperature\n2.Angle\n3.Distance\n4.Time\n");
printf("\nEnter option\t");
scanf("%d",&option);
switch(option)
{
case 1:
clrscr();
printf("Temperature\n");
printf("\n1.Celsius\n2.Fahrenheit\n3.Kelvin\n");
scanf("%d",&option);
switch(option)
{
case 1:
clrscr();
printf("Celsius\n");
printf("\nEnter temperature in celsius\t");
scanf("%f",&z);
x=1.8*z+32;
y=z+273.15;
printf("\n%0.2f C = %0.2f F\n",z,x);
printf("%0.2f C = %0.2f K\n",z,y);
break;
case 2:
clrscr();
printf("Fahrenheit\n");
printf("\nEnter temperature in fahrenheit\t");
scanf("%f",&x);
y=((x+459.67)*5)/9;
z=0.5556*(x-32);
printf("\n%0.2f F = %0.2f C\n",x,z);
printf("%0.2f F = %0.2f K\n",x,y);
break;
case 3:
clrscr();
printf("Kelvin\n");
printf("\nEnter temperature in kelvin\t");
scanf("%f",&x);
y=x-273.15;
z=(x*1.8)-459.67;
printf("\n%0.2f K = %0.2f C\n",x,y);
printf("%0.2f K = %0.2f F\n",x,z);
break;
}
break;
case 2:
clrscr();
printf("Angle\n");
printf("\n1.Degree\n2.Radian\n3.Gradian\n");
printf("\nEnter option\t");
scanf("%d",&option);
switch(option)
{
case 1:
clrscr();
printf("Degree\n");
printf("\nEnter angle in degree\t");
scanf("%d",&a);
x=a*pi/180;
y=a*1.111;
printf("%d degree = %0.3f radian\n",a,x);
printf("%d degree = %0.3f gradian\n",a,y);
break;
case 2:
clrscr();
printf("Radian\n");
printf("\nEnter angle in radian\t");
scanf("%d",&a);
x=a*180/pi;
y=a*63.662;
printf("%d radian = %0.3f degree\n",a,x);
printf("%d radian = %0.3f gradian\n",a,y);
break;
case 3:
clrscr();
printf("Gradian\n");
printf("\nEnter angle in gradian\t");
scanf("%d",&a);
x=a*0.9;
y=a*0.0157;
printf("%d gradian = %0.3f degree\n",a,x);
printf("%d gradian = %0.3f radian\n",a,y);
break;
}
break;
case 3:
clrscr();
printf("Length\n");
printf("\n1.Metre\n2.Feet\n3.Inch\n");
printf("\nEnter option\t");
scanf("%d",&option);
switch(option)
{
case 1:
clrscr();
printf("Metre\n");
printf("\nEnter length in metre\t");
scanf("%d",&a);
x=a*3.280;
y=a*39.37;
printf("%d metre = %0.3f feet\n",a,x);
printf("%d metre = %0.3f inch\n",a,y);
break;
case 2:
clrscr();
printf("Feet\n");
printf("\nEnter length in feet\t");
scanf("%d",&a);
x=a*0.3048;
y=a*12;
printf("%d feet = %0.3f metre\n",a,x);
printf("%d feet = %0.3f inch\n",a,y);
break;
case 3:
clrscr();
printf("Inch\n");
printf("\nEnter length in inch\t");
scanf("%d",&a);
x=a*0.0254;
y=a*0.0833;
printf("%d inch = %0.3f metre\n",a,x);
printf("%d inch = %0.3f feet\n",a,y);
break;
}
break;
case 4:
clrscr();
printf("Time\n");
printf("\n1.Second\n2.Minute\n3.Hour\n");
printf("\nEnter option\t");
scanf("%d",&option);
switch(option)
{
case 1:
clrscr();
printf("Second\n");
printf("\nEnter time in second\t");
scanf("%d",&a);
x=a/60;
y=a*3600;
printf("%d second = %0.3f minute\n",a,x);
printf("%d second = %0.3f hour\n",a,y);
break;
case 2:
clrscr();
printf("Minute\n");
printf("\nEnter time in minute\t");
scanf("%d",&a);
x=a*60;
y=a/60;
printf("%d minute = %0.3f second\n",a,x);
printf("%d minute = %0.3f hour\n",a,y);
break;
case 3:
clrscr();
printf("Hour\n");
printf("\nEnter time in hour\t");
scanf("%d",&a);
x=a*3600;
y=a*60;
printf("%d hour = %0.3f second\n",a,x);
printf("%d hour = %0.3f minute\n",a,y);
break;
}
break;
}
break;
case 4:
clrscr();
printf("\nMensuration\n");
printf("1.Square\n2.Rectangle\n3.Circle\n4.Cube\n");
printf("5.Cuboid\n6.Sphere\n7.Hemisphere\n8.Cylinder\n");
printf("9.Cone\t\n10.Equilateral Triangle\n11.Isosceles Triangle\n12.Scalene Triangle\n13.Right Angled Triangle\n");
printf("\n\nEnter option\t");
scanf("%d",&option);
switch(option)
{
case 1:
clrscr();
printf("\nSquare\n");
printf("Enter side\t");
scanf("%d",&a);
b=a*a;
c=4*a;
x=sqrt(2)*a;
printf("Side = %d\n",a);
printf("Area = side x side = %d\n",b);
printf("Perimeter = 4 x side = %d\n",c);
printf("Length of diagonal=%0.3f",x);
break;
case 2:
clrscr();
printf("Rectangle\n");
printf("Enter length and breadth\t");
scanf("%d%d",&a,&b);
printf("Length (l)=%d\n",a);
printf("Breadth (b)=%d\n",b);
c=a*b;
c1=2*(a+b);
x=sqrt(pow(a,2)+pow(b,2));
printf("Area=lxb=%d\n",c);
printf("Perimeter=2(l+b)=%d\n",c1);
printf("Length of diagonal=%0.3f\n",x);
break;
case 3:
clrscr();
printf("\nCircle\n");
printf("Enter radius\t");
scanf("%d",&a);
x=pi*a*a;
y=2*pi*a;
printf("Area=%0.2f\n",x);
printf("Circumference=%0.2f\n",y);
break;
case 4:
clrscr();
printf("\nCube\n");
printf("Enter side\t");
scanf("%d",&a);
b=pow(a,3);
c=4*pow(a,2);
c1=6*pow(a,2);
x=a*sqrt(3);
printf("\nLength of face = %d\n",a);
printf("Volume = %d\n",b);
printf("Lateral surface area = %d\n",c);
printf("Total surface area = %d\n",c1);
printf("Length of diagonal = %0.2f\n",x);
break;
case 5:
clrscr();
printf("\nCuboid\n");
printf("Enter length,breadth and height\t");
scanf("%d%d%d",&a,&b,&c);
c1=a*b*c;
c2=2*c*(a+b);
c3=2*(a*b+b*c+a*c);
x=sqrt(pow(a,2)+pow(b,2)+pow(c,2));
printf("\nLength (l) = %d\n",a);
printf("Breadth (b) = %d\n",b);
printf("Height (h) = %d\n",c);
printf("Volume = lxbxh = %d\n",c1);
printf("Lateral surface area = %d\n",c2);
printf("Total surface area = %d\n",c3);
printf("Length of diagonal = %0.2f\n",x);
break;
case 6:
clrscr();
printf("\nSphere\n");
printf("Enter radius\t");
scanf("%d",&a);
x=(4*pi*pow(a,3))/3;
y=4*pi*pow(a,2);
printf("Volume = %0.2f\n",x);
printf("Surface area = %0.2f\n",y);
break;
case 7:
clrscr();
printf("\nHemisphere\n");
printf("Enter radius\t");
scanf("%d",&a);
x=(2*pi*pow(a,3))/3;
y=2*pi*pow(a,2);
printf("Volume = %0.2f\n",x);
printf("Surface area = %0.2f\n",y);
break;
case 8:
clrscr();
printf("\nCylinder\n");
printf("Enter radius\t");
scanf("%d",&a);
printf("Enter height\t");
scanf("%d",&b);
x=pi*pow(a,2)*b;
y=2*pi*a*b;
z=2*pi*a*(a+b);
printf("Volume = %0.2f\n",x);
printf("Curved surface area = %0.2f\n",y);
printf("Total surface area = %0.2f\n",z);
break;
case 9:
clrscr();
printf("\nCone\n");
printf("Enter radius\t");
scanf("%d",&a);
printf("Enter height\t");
scanf("%d",&b);
x=(pi*pow(a,2)*b)/3;
z1=sqrt(pow(a,2)+pow(b,2));
y=pi*a*z1;
z=pi*a*(a+z1);
printf("Volume = %0.2f\n",x);
printf("Slant height = %0.2f\n",z1);
printf("Curved surface area = %0.2f\n",y);
printf("Total surface area = %0.2f\n",z);
break;
case 10:
clrscr();
printf("Equilateral Triangle\n");
printf("Enter side\t");
scanf("%d",&a);
x=(sqrt(3)*pow(a,2))/4;
b=3*a;
y=(sqrt(3)*a)/2;
printf("Area=%0.2f\n",x);
printf("Perimeter=%d\n",b);
printf("Height=%0.2f\n",y);
break;
case 11:
clrscr();
printf("Isosceles Triangle\n");
printf("Enter sides 1 & 2\t");
scanf("%d",&a);
printf("Enter side 3\t");
scanf("%d",&b);
x=(b*sqrt(4*pow(a,2)-pow(b,2))/4);
c=2*a+b;
printf("Area=%0.2f\n",x);
printf("Perimeter=%d\n",c);
break;
case 12:
clrscr();
printf("Scalene Triangle\n");
printf("Enter side 1\t");
scanf("%d",&a);
printf("Enter side 2\t");
scanf("%d",&b);
printf("Enter side 3\t");
scanf("%d",&c);
z=(a+b+c)/2;
x=sqrt(z*(z-a)*(z-b)*(z-c));
c2=a+b+c;
printf("Area=%0.2f\n",x);
printf("Perimeter=%d\n",c2);
break;
case 13:
clrscr();
printf("Right Angled Triangle\n\n");
printf("Enter base\t");
scanf("%d",&a);
printf("Enter height\t");
scanf("%d",&b);
x=0.5*a*b;
y=sqrt(pow(a,2)+pow(b,2));
z=a+b+y;
printf("Area=%0.3f",x);
printf("\nLength of hypotenuse=%0.3f",y);
printf("\nPerimeter=%0.3f",z);
break;
}
break;
}
getch();
return 0;
}
