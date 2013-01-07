#include<stdio.h>
#include<conio.h>
#include<alloc.h>
void main(void)
{
int a[10][10],b[10][10],c[10][10];
int m,n,p,q,i,j,k;
clrscr();
printf("Enter the size of matrix A as m,n:");
scanf("%d %d",&m,&n);
printf("Enter the size of matrix B as p,q:");
scanf("%d %d",&p,&q);
 printf("---------------------------------------\n");
if((m>10)||(n>10)||(p>10)||(q>10))
{
printf("Matrix of size more then declared\n");
 exit(1);
}
if(n!=p)
{
printf("matrix product A*B is not possible\n");
 exit(1);
}
	printf("Enter elements of matrix A row wise\n");
 for(i=0;i<m;i++)
 for(j=0;j<n;j++)
 scanf("%d",&a[i][j]);
	printf("Enter the elements of matrix B row wise \n");
 for(i=0;i<p;i++)
 for(j=0;j<q;j++)
 scanf("%d",&b[i][j]);
 printf("product A*B matrix C is:\n");
 for(i=0;i<m;i++)
 {
 for(j=0;j<q;j++)
 {
 c[i][j]=0;
 for(k=0;k<n;k++)
 c[i][j]+=a[i][k]*b[k][j];
 }
	}
for(i=0;i<m;i++)
{
for(j=0;j<q;j++)
printf("%d",c[i][j]);
printf("\n");
}
getch();
}


