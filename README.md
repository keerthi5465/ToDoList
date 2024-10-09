### Description:
This C program is a basic To-Do List Manager that lets users create categories and tasks within those categories. Users can add categories, add tasks to categories, delete tasks, display tasks by category, and count the total number of tasks. The data structure used is a singly linked list for both categories and tasks.

## Data Structures:
Category: Represents a to-do list category, containing a category_name and a linked list of tasks.

Copy code
```
struct category {
    char category_name[100];
    struct task* tasks;
    struct category* next;
};
```
Task: Represents an individual task within a category.


Copy code
```
struct task {
    char task_about[100];
    struct task* next;
};
```
Functions:
create_task: Creates a new task node and initializes it with a task description.

c
Copy code
```
struct task* create_task(const char* task_about);
```
create_category: Creates a new category node and initializes it with a category name.

c
Copy code
```
struct category* create_category(const char* category_name);
```
find_category: Searches for a category by name in the linked list of categories.

c
Copy code
```
struct category* find_category(struct category* head, const char* category_name);
```
add_task: Adds a new task to a given category.

c
Copy code
```
void add_task(struct category* category_name, const char* task_about);
```
delete_task: Deletes a task from a given category by its task description.

c
Copy code
```
void delete_task(struct category* category_name, const char* task_about);
```
count_task: Counts the total number of tasks across all categories.

c
Copy code
```
int count_task(struct category* head);
```
display_task_by_category: Displays tasks categorized by their category names.

c
Copy code
```
void display_task_by_category(struct category* head);
```
## Main Menu:
The program operates through a menu-driven interface with six options:

1. Add Category: Adds a new category to the list.
2. Add Task: Adds a task to a selected category.
3. Delete Task: Deletes a task from a selected category.
4. Display Categories and Tasks: Displays all categories and their associated tasks.
5. Count Total Tasks: Displays the total number of tasks across all categories.
