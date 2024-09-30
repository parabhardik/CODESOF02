# CODESOF02
# To-Do List Program

tasks = []

while True:
    print("\nOptions:")
    print("1. Add task")
    print("2. Delete task")
    print("3. Mark task as done")
    print("4. Display tasks")
    print("5. Quit")
    choice = input("Enter your choice: ")

    if choice == "1":
        task = input("Enter a new task: ")
        tasks.append(task)
        print(f"Task '{task}' added!")
    elif choice == "2":
        if tasks:
            print("Tasks:")
            for i, task in enumerate(tasks, start=1):
                print(f"{i}. {task}")
            task_number = int(input("Enter the task number to delete: ")) - 1
            if task_number < len(tasks):
                del tasks[task_number]
                print("Task deleted!")
            else:
                print("Invalid task number!")
        else:
            print("No tasks to delete!")
    elif choice == "3":
        if tasks:
            print("Tasks:")
            for i, task in enumerate(tasks, start=1):
                print(f"{i}. {task}")
            task_number = int(input("Enter the task number to mark as done: ")) - 1
            if task_number < len(tasks):
                tasks[task_number] = f"[DONE] {tasks[task_number]}"
                print("Task marked as done!")
            else:
                print("Invalid task number!")
        else:
            print("No tasks to mark as done!")
    elif choice == "4":
        if tasks:
            print("Tasks:")
            for i, task in enumerate(tasks, start=1):
                print(f"{i}. {task}")
        else:
            print("No tasks!")
    elif choice == "5":
        break
    else:
        print("Invalid choice!")
