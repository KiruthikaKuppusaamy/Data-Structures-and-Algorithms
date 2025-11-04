// Circular Linked List

#include <stdio.h>
#include <stdlib.h>

int choice, value;

struct Node 
{
    int data;
    struct Node *next;
};

struct Node *head = NULL;

// Insert at End
void insertEnd() 
{
    struct Node *newNode = malloc(sizeof(struct Node));
    
    printf("Enter value: ");
    scanf("%d", &value);
    
    newNode->data = value;

    if (head == NULL) 
    {  
        head = newNode;
        newNode->next = head;   // Points to itself
      }

    struct Node *temp = head;
    while (temp->next != head)  // Traverse till last node
        temp = temp->next;

    temp->next = newNode;
    newNode->next = head;

    printf("%d inserted.\n", value);
}

// Delete from Front
void deleteFront() 
{
    if (head == NULL) 
    {
        printf("List is empty!\n");
        exit(0);
    }

    struct Node *temp = head;

    // Only one node
    if (head->next == head) 
    {
        printf("%d deleted.\n", head->data);
        free(head);
        head = NULL;
        return;
    }

    struct Node *last = head;
    while (last->next != head)
        last = last->next;

    head = head->next;
    last->next = head;

    printf("%d deleted.\n", temp->data);
    free(temp);
}

// Display
void display() 
{
    if (head == NULL) 
    {
        printf("List is empty!\n");
        return;
    }

    struct Node *temp = head;
    printf("Circular List: ");

    do 
    {
        printf("%d -> ", temp->data);
        temp = temp->next;
    } while (temp != head);

    printf("(back to head)\n");
}

void main() 
{
    while (1) 
    {
        printf("\n--- Circular Linked List Menu ---\n");
        printf("1. Insert at End\n");
        printf("2. Delete Front\n");
        printf("3. Display\n");
        printf("4. Exit\n");
        printf("Enter choice: ");
        scanf("%d", &choice);

        switch (choice)
        {
            case 1:
                insertEnd();
                break;
            case 2:
                deleteFront();
                break;
            case 3:
                display();
                break;
            case 4:
                exit(0);
            default:
                printf("Invalid choice!\n");
        }
    }
}
