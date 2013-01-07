#include<stdio.h>
#include<conio.h>
typedef struct node_type
{
int info;
struct node_type *next;
}
node;

void create_empty_list(node **head)
 {
  *head=(node *)NULL;
 }

  node *search(node *head,int item)
 {
 while( head!=(node *) NULL)
 {
 if(head->info==item)
  return head;
  head=head->next;
  }
  return NULL;
 }

 void insert_at_beginning(node **head,int item)
{
 node *ptr;
 ptr=(node *)malloc(sizeof(node));
 ptr->info=item;
 if(*head==(node * )NULL)
 ptr->next=(node * )NULL;
 else
 ptr->next= * head;
 *head = ptr ;
 }

 void insert_at_end(node **head,int item)
{
node *ptr,*loc;
ptr=(node *)malloc(sizeof(node));
ptr->info=item;
ptr->next=(node *)NULL;
if(*head==(node *)NULL)
*head=ptr;
else
{
loc= *head;
while(loc->next!=(node *)NULL)
loc=loc->next;
loc->next=ptr;
}
}

 void insert_after_element(node *head,int item,int after)
{
node *ptr,*loc;
loc = search(head,after);
if(loc==(node *)NULL)
return;
ptr=(node *)malloc(sizeof (node));
ptr->info=item;
ptr->next=loc->next;
loc->next = ptr;
}

 void traverse_in_order(node *head)
 {
 while (head!=(node *)NULL)
 {
 printf("%d\n",head->info);
 head=head->next;
 }
 }

 void traverse_in_reverse_order_2(node *head)
 {
 if(head->next!=(node *)NULL)
 traverse_in_reverse_order_2(head->next);
 printf("%d\n",head->info);
 }

 void delete_at_beginning(node **head)
 {
 node *ptr;
 if(*head ==(node *) NULL)
 return;
 else
 {
 ptr = *head;
 *head = (*head)->next;
 free(ptr);
 }
 }

 void delete_at_end(node **head)
 {
 node *ptr,*loc;
 if(*head==(node*) NULL)
 return;
 else if ((*head)->next==(node *)NULL)
 {
 ptr=*head;
 *head=(node *)NULL;
 free(ptr);
 }
 else
 {
 loc= *head;
 ptr = (*head)->next;
 while(ptr->next!=(node *)NULL)
 {
 loc=ptr;
 ptr=ptr->next;
 }
 loc->next=(node *)NULL;
 free(ptr);
 }
 }
void delete_after_element(node *head ,int after)
{
node *ptr , *loc;
loc = search(head,after);
if(loc==(node *)NULL)
return;
ptr=loc->next;
loc->next=ptr->next;
free(ptr);
}
void delete_list(node **head)
{
node *ptr;
while(*head!=(node *) NULL)
{
ptr= *head;
*head =(*head)->next;
free(ptr);
}
}
void main(void)
{
node *head;
int choice, element,after;
create_empty_list(&head);
while(1)
{
clrscr();
printf("options available");
printf("==============================\n");
printf("	1. Insert at beginning\n");
printf("	2. Insert at end \n");
printf("	3. Insert after element\n");
printf("	4. Traverse in order\n");
printf("	5. Traverse in reverse order\n");
printf("	6. Delete from beginning\n");
printf("	7. Delete from end\n");
printf("	8. Delete after a given element\n");
printf(" 	9. Delete list\n");
printf("       10. Exit\n");
printf("Enter your choice(1-10)\n");
scanf("%d",&choice);
clrscr();
switch(choice)
{
case 1: printf("Enter element:");
scanf("%d",&element);
insert_at_beginning(&head,element);
break;
case 2: printf("Enter Element:");
scanf("%d",&element);
insert_at_end(&head,element);
break;
case 3: printf("Enter Element:");
scanf("%d",&element);
printf("enter element after which to insert");
scanf("%d",&after);
insert_after_element(head,element,after);
break;
case 4 : if(head == (node *)NULL)
printf("list is empty...");
else
traverse_in_order(head);
printf("\n press any key to continue");
getch();
break;
case 5: if(head==(node *)NULL)
printf("list is empty..");
else
traverse_in_reverse_order_2(head);
printf("press any key to continue");
getch();
break;
case 6:
delete_at_beginning(&head);
break;
case 7: delete_at_end(&head);
break;
case 8: printf("enter element after which to delete:");
scanf("%d",&after);
delete_after_element(head,after);
break;
case 9:
delete_list(&head);
break ;
case 10:
exit();
}
}
}
