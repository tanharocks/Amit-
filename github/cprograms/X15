#include<stdio.h>
#include<conio.h>
typedef struct node_type
{
struct node_type *prev;
int info;
struct node_type *next;
}
node;
node *head,*tail;
void create_empty_list(node **head,node **tail)
{
*head=*tail=(node *)NULL;
}
void traverse_in_order(node *head)
{
while(head!=(node *)NULL)
{
printf("%d  ",head->info);
head=head->next;
}
}
void traverse_in_reverse_order(node *tail)
{
while(tail!= ( node *) NULL)
{
printf("%d  ",tail->info);
tail=tail->prev;
}
}
 node *search(node *head,int item)
{
while(head!=(node *)NULL)
{
if(head->info==item)
return head;
head=head->next;
}
return NULL;
}
void insert_at_beginning(node **head,node **tail,int item)
{
node *ptr;
ptr=(node *)malloc(sizeof(node));
ptr->info=item;
if(*head==(node *)NULL)
{
ptr->prev = ptr->next =(node *)NULL;
*head=*tail=ptr;
}
else
{
ptr->prev=(node *)NULL;
ptr->next=*head;
*head=ptr;
}
}
void insert_at_end(node **head,node **tail,int item)
{
node *ptr;
ptr = (node *)malloc(sizeof(node));
ptr->info=item;
if(*head==(node *)NULL)
{
ptr->prev=ptr->next= (node *)NULL;
*head= *tail=ptr;
}
else
{
ptr->next= (node *)NULL;
ptr->prev= *tail;
(*tail)->next=ptr;
*tail=ptr;
 }
 }
 void insert_before_element(node **head,int item,int before)
 {
 node *ptr,*loc;
 ptr= *head;
 loc=search(ptr,before);
 if(loc==(node *)NULL)
return;
ptr=(node *)malloc(sizeof(node));
ptr->info=item;
if(loc->prev==(node *)NULL)
{
ptr->prev=(node *)NULL;
loc->prev=ptr;
ptr->next=*head;
*head=ptr;
}
else
{
ptr->prev=loc->prev;
ptr->next=loc;
(loc->prev)->next=ptr;
loc->prev=ptr;
}
}
void insert_after_element(node **head,node **tail,int item,int after)
{
node *ptr,*loc;
ptr=*head;
loc=search(ptr,after);
if(loc==(node *)NULL)
return;
ptr=(node *)malloc(sizeof(node));
ptr->info=item;
if(loc->next==(node *)NULL)
{
ptr->next=(node *)NULL;
loc->next=ptr;
ptr->prev=*tail;
*tail=ptr;
}
else
{
ptr->prev=loc;
ptr->next=loc->next;
(loc->next)->prev=ptr;
loc->next=ptr;
}
}
void delete_at_beginning(node **head,node **tail)
{
node *ptr;
if(*head==(node *)NULL)
return;
else if((*head)->next == (node *)NULL)
{
ptr= *head;
*head= *tail=(node *)NULL;
free(ptr);
}
else
{
ptr = *head;
*head= (*head)->next;
(*head)->prev=(node *)NULL;
free(ptr);
}
}
void delete_at_end(node **head,node **tail)
{
node *ptr;
if(*head==(node *)NULL)
return;
else if ((*head)->next==(node *)NULL)
{
ptr=*head;
*head= *tail=(node *)NULL;
free(ptr);
}
else
{
ptr= *tail;
*tail=(*tail)->prev;
(*tail)->next=(node *)NULL;
free(ptr);
}
}
void delete_after_element(node **head,node **tail,int after)
{
node *ptr,*loc;
ptr=*head;
loc=search(ptr,after);
if(loc==(node *)NULL)
return;
else if ((loc->next)->next==(node *)NULL)
{
ptr =loc->next;
loc->next=(node *)NULL;
*tail=loc;
free(ptr);
}
else
{
ptr=loc->next;
loc->next=ptr->next;
(ptr->next)->prev=loc;
free(ptr);
}
}
void delete_before_element(node **head,node **tail,int before)
{
node *ptr,*loc;
ptr= *head;
loc=search(ptr,before);
if(loc==(node *)NULL)
return;
else if ((loc->prev)->prev==(node *)NULL)
{
 ptr=loc->prev;
loc->prev=(node *)NULL;
*head=loc;
free(ptr);
}
else
{
ptr=loc->prev;
loc->prev=ptr->prev;
(ptr->prev)->next=loc;
free(ptr);
}
}

void delete_list(node **head,node **tail)
{
node *ptr;
while(*head!=(node *)NULL)
{
ptr= *head;
*head=(*head)->next;
free(ptr);
}
*tail=(node *)NULL;
}
void main(void)
{
int choice,element,after,before;
node *head,*tail;
create_empty_list(&head,&tail);
while(1)
{
clrscr();
printf("Options available .\n");
printf("=============================\n");
printf(" 1.  Insert at beginning.\n");
printf(" 2.  Insert at end.\n");
printf(" 3.  Insert After given element.\n");
printf(" 4.  Insert brfore given element.\n");
printf(" 5.  Traverse in order.\n");
printf(" 6.  Traverse in reverse order.\n");
printf(" 7.  Delete at beginning.\n");
printf(" 8.  Delete at end.\n");
printf(" 9.  Delete after given element\n");
printf("10.  Delete before a given element.\n");
printf("11.  Delete List.\n");
printf("12.  Exit.\n");
printf("\n Enter choice.\n");
scanf("%d",&choice);
clrscr();
switch(choice)
{
case 1: clrscr();
printf("\n Enter element:");
scanf("%d",&element);
insert_at_beginning(&head,&tail,element);
break;
case 2:
printf("\n Enter element.");
scanf("%d",&element);
insert_at_end(&head,&tail,element);
break;
case 3: printf("\n enter element.");
scanf("%d",&element);
printf("\n Enter element , after which to insert");
scanf("%d",&after);
insert_after_element(&head,&tail,element,after);
break;
case 4:
printf("\n Enter element.");
scanf("%d",&element);
printf("\n enter element before which to insert:");
scanf("%d",&before);
insert_before_element(&head,element,before);
break;
case 5: if(head==(node *)NULL)
printf("\n list is empty.");
traverse_in_order(head);
printf("\n press any key to continue");
getch();
break;
case 6: if(head==(node *)NULL)
printf("\n list is empty .");
traverse_in_reverse_order(tail);
printf("\n press any key to continue");
getch();
break;
case 7: delete_at_beginning(&head,&tail);
break;
case 8: delete_at_end(&head,&tail);
break;
case 9: printf("\nEnter element after which to delete\n");
scanf("%d",&after);
delete_after_element(&head,&tail,after);
break;
case 10: printf("\nenter element before which to delete:\n");
scanf("%d",&before);
delete_before_element(&head,&tail,before);
break;
case 11: delete_list(&head,&tail);
break;
case 12: exit(1);
}
}
}



