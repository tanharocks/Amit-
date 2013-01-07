#include<stdio.h>
#include<conio.h>
#define MAX 100
#define NIL -1
typedef struct
{
int top;
int elements[MAX];
}stack_type;
void main(void)
{
int choice,x;
stack_type stack;
void create_stack(stack_type *);
int isempty(stack_type *);
int isfull(stack_type *);
void push(stack_type *,int);
int pop(stack_type *);
create_stack(&stack);
do
{
clrscr();
printf("options availables \n");
printf("++++++++++++++++++++++++++++\n");
printf("  1. Push \n");
printf("2. Pop\n");
printf("3. Exit \n");
printf("Enter your chioice(1-3)");
scanf("%d",&choice);
switch(choice)
{
case 1: clrscr();
if(isfull(&stack))
{
printf("stack is full ,press any key to continue");
getch();
}
 else
 {
 printf("enter value:");
 scanf("%d",&x);
 push(&stack,x);
 }
 break;
 case 2: clrscr();
 if(isempty(&stack))
 {
 printf("stack is empty,press any key to continue");
 getch();
 }
 else
 {
 printf("value poped is%d\n",pop(&stack));
 printf("press any key to continue");
	getch();
 }
 }
 }
 while(choice!=3);
 }

 void create_stack(stack_type *v)
 {
 v->top=NIL;
 }
 int isempty(stack_type *v)
 {
 if(v->top==-1)
 return 1;
 else
 return 0;
 }
 int isfull(stack_type *v)
 {
 if(v->top==(MAX-1))
 return 1;
 else
 return 0;
 }
 void push(stack_type *v, int value)
 {
 v->elements[++v->top] = value;
 }
 int pop(stack_type *v)
 {
 return(v->elements[v->top--]);
 }
