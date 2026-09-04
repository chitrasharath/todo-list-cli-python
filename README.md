# Todo List CLI

A simple command-line todo list application written in Python. Tasks are kept
in memory while the application is running and can be saved to or loaded from
`todos.csv`.

## Requirements

- Python 3

## Run the application

From the repository directory, run:

```bash
python3 app.py
```

Use the menu to:

1. Add a task
2. Delete a task by its number
3. Print the current task list
4. Save tasks to `todos.csv`
5. Load tasks from `todos.csv`
6. Exit

The CSV file is created in the current working directory when tasks are saved.
Loading replaces the current in-memory list with the tasks in `todos.csv`.

## Run the tests

```bash
python3 -m unittest test.py
```

The task operations are also available as functions when importing `app`:

```python
from app import add_one_task, delete_task, get_todos, load_todos, save_todos

add_one_task("Buy groceries")
delete_task(1)
save_todos()
load_todos()
print(get_todos())
```
