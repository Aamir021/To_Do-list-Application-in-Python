# To_Do-list-Application-in-Python

# Task list
todo_list = []

# Function to add a task
def add_task(task):
    todo_list.append({"task": task, "completed": False})
    print(f"Task added: {task}")

# Function to delete a task
def delete_task(index):
    if 0 <= index < len(todo_list):
        removed = todo_list.pop(index)
        print(f"Task deleted: {removed['task']}")
    else:
        print("Invalid task number.")

# Function to display tasks
def display_tasks():
    if not todo_list:
        print("No tasks in the list.")
    else:
        print("\nTo-Do List:")
        for i, task in enumerate(todo_list):
            status = "✓" if task["completed"] else "✗"
            print(f"{i}. [{status}] {task['task']}")
        print()

# Function to mark a task as complete
def complete_task(index):
    if 0 <= index < len(todo_list):
        todo_list[index]["completed"] = True
        print(f"Task marked as complete: {todo_list[index]['task']}")
    else:
        print("Invalid task number.")

# Using Function
add_task("Play Games")
add_task("Study Python")
display_tasks()
complete_task(1)
delete_task(0)
display_tasks()

