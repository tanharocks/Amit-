#include<stdio.h>
#include<conio.h>
void main(void)
{
int ncr,n,r;//program binomial coefficient
int factorial(int k);
clrscr();
printf("Enter the value of n:");
scanf("%d",&n);
printf("enter value of r:");
scanf("%d",&r);
ncr= factorial(n)/(factorial(r)* factorial(n-r));
printf("value of ncr: %d",ncr);
getch();
}
int factorial(int k)
{
int product=1,i;
for(i=2;i<=k;i++)
product*=i;
return product;
}