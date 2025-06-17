# TO _ DO APPLICATION IN PYTHON

# Objective

We have to create a small program in Python where:
•	We can add, delete, view, and mark tasks as complete.
•	We'll use functions and data structures like lists and dictionaries.

# Step 1: Create an Empty To-Do List :

	 We create an empty list called todo_list to store all the tasks.
 Example: 	todo_list = []
# Step 2: Add a Task Function :
 We define a function that allows us to add a task.
Example:  def add_task(task):
  		  todo_list.append({"task": task, "completed": False})
    		  print("Task added: {task}")
        
What it does :

Takes a task name like "Buy milk" as input.
Adds it to the list with a tag completed: False.
Displays a message that task is added.
OUTPUT : 	add_task("Buy milk")

# Step 3: Display All Tasks :

We want to show all tasks on the screen.
Example : 
def display_tasks():
if not todo_list:
print("No tasks in the list.")
else:
print("\nTo-Do List:")
for i, task in enumerate(todo_list):
status = "✓" if task["completed"] else "✗"
print("{i}. [{status}] {task['task']}")
print()

What it does :

If list is empty → shows message.
If not → shows each task with a number and whether it is completed (✓) or not (✗).
OUTPUT : 
To-Do List:
0. [✗] Buy milk
1. [✓] Study Pytho

# Step 4: Mark a Task as Complete :
We create a function to mark a task as done.
Example :
def complete_task(index):
if 0 <= index < len(todo_list):
todo_list[index]["completed"] = True
print("Task marked as complete: {todo_list[index]['task']}")
else:
print("Invalid task number.")

What it does :

Takes the task index (number).
Changes "completed": False to "completed": True.

Use Function
complete_task(0)

# Step 5: Delete a Task :

Let’s make a function to delete/remove a task.
Example :
def delete_task(index):
if 0 <= index < len(todo_list):
removed = todo_list.pop(index)
print("Task deleted: {removed['task']}")
else:
print("Invalid task number.")

What it does :
Takes task number.
Removes that task from the list using .pop().
Shows message that task is deleted.

Use Function
delete_task(1)



# Step 6: Try All Functions Together :

add_task("Buy milk")
add_task("Study Python")
display_tasks()
complete_task(1)
display_tasks()
delete_task(0)
display_tasks()
