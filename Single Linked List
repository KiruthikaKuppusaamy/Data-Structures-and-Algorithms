#include <stdio.h>
#include <stdlib.h>

int choice, value;

// structure for a node
struct Node 
{
    int data;
    struct Node *next;
};

// head pointer
struct Node *head = NULL; 

// function to insert a node at the end
void insertEnd() 
{
    
    printf("Enter value to insert: ");
    scanf("%d", &value);
    
    struct Node *newNode = (struct Node *)malloc(sizeof(struct Node));
    newNode->data = value;
    newNode->next = NULL;

    if (head == NULL) 
    {
        head = newNode;
    } else 
    {
        struct Node *temp = head;
        while (temp->next != NULL)
            temp = temp->next;
        temp->next = newNode;
    }
    printf("%d inserted into the list.\n", value);
}

// Function to delete the first node
void deleteFront() 
{
    if (head == NULL) 
    {
        printf("List is empty!\n");
        return;
    }
    struct Node *temp = head;
    head = head->next;
    printf("%d deleted from the list.\n", temp->data);
    free(temp);
}

// Function to display the list
void display() 
{
    if (head == NULL) 
    {
        printf("List is empty!\n");
        return;
    }
    struct Node *temp = head;
    printf("List elements: ");
    while (temp != NULL) 
    {
        printf("%d ", temp->data);
        temp = temp->next;
    }
    printf("\n");
}

// Main function
void main() 
{
    

    while (1) 
    {
        printf("\n--- Linked List Implementation ---\n");
        printf("1. Insert at End\n2. Delete from Front\n3. Display\n4. Exit\n");
        printf("Enter your choice: ");
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
