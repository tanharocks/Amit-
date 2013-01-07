#include<stdio.h>
#include<conio.h>
#define NIL -1
#define MAX 100
typedef struct
{
int front;
int rear;
int elements[MAX];
}
queue_type;
void main(void)
{
int choice ,n,x;
queue_type queue;
int i;
void create_queue(queue_type *);
int isempty(queue_type *);
int isfull(queue_type *);
void enqueue(queue_type *, int);
int dequeue(queue_type *);
create_queue(&queue);
do
{
clrscr();
printf("options available\n");
printf("+++++++++++++++++++++++++++\n");
printf(" 1. Enqueue \n");
printf(" 2. Dequeue \n");
printf(" 3. Exit \n");
printf("enter your choice(1-3):");
scanf("%d",&choice);
switch(choice)
{
case 1: clrscr();
if(isfull(&queue))
{
printf("Queue is full...\n press any key to continue ");
getch();
}
else
{
printf("enter value");
scanf("%d",&x);
enqueue(&queue,x);
}
break;
case 2: clrscr();
if(isempty(&queue))
{
printf("Queue Empty \n press any key to continue ");
getch();
}
else
{
printf("value dequeuedid %d \n",dequeue(&queue));
printf("press any key to continue");
getch();
}
}}while(choice!=3);
}
void create_queue(queue_type *v)
{
v->front=v->rear==NIL;
}
int isempty(queue_type *v)
{
if(v->front==NIL)
return 1;
else
return 0;
}
int isfull(queue_type *v)
{
if((v->front==0)&& (v->rear==(MAX-1)))
return 1;
else
return 0;
}
void enqueue(queue_type *v,int x)
{
if(v->front==NIL)
v->front=v->rear=0;
else if(v->rear==(MAX-1))
v->rear=0;
else
v->rear++;
v->elements[v->rear] = x;
}
int dequeue(queue_type *v)
{
int temp;
temp=v->elements[v->front];
if(v->front==v->rear)
v->front=v->rear=NIL;
else
v->front++;
return temp;
}
