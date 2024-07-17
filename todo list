#include <stdio.h>
#include <string.h>

#define MAX_TASKS 100
#define MAX_TASK_LEN 50

int main() {
    char tasks[MAX_TASKS][MAX_TASK_LEN];
    int numTasks = 0;

    int choice;

    while (1) {
        printf("\nTo-Do List\n");
        printf("1. Add task\n");
        printf("2. View tasks\n");
        printf("3. Remove task\n");
        printf("4. Mark task as complete\n");
        printf("5. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                if (numTasks < MAX_TASKS) {
                    printf("Enter task: ");
                    scanf("%s", tasks[numTasks]);
                    numTasks++;
                } else {
                    printf("To-do list is full.\n");
                }
                break;
            case 2:
                if (numTasks == 0) {
                    printf("No tasks.\n");
                } else {
                    printf("Tasks:\n");
                    for (int i = 0; i < numTasks; i++) {
                        printf("%d. %s\n", i + 1, tasks[i]);
                    }
                }
                break;
            case 3:
                if (numTasks == 0) {
                    printf("No tasks to remove.\n");
                } else {
                    int index;
                    printf("Enter task number to remove: ");
                    scanf("%d", &index);
                    if (index >= 1 && index <= numTasks) {
                        for (int i = index - 1; i < numTasks - 1; i++) {
                            strcpy(tasks[i], tasks[i + 1]);
                        }
                        numTasks--;
                    } else {
                        printf("Invalid task number.\n");
                    }
                }
                break;
            case 4:
                // Implement marking tasks as complete
                break;
            case 5:
                printf("Exiting...\n");
                return 0;
            default:
                printf("Invalid choice.\n");
        }
    }

    return 0;
}
