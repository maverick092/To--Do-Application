# To-Do List Application

A Python-based, menu-driven To-Do List Application developed as part of my InfozaTech Python internship tasks. It helps users organize tasks, track completion, assign priorities, and set due dates.

## Features

- **Add tasks** with a description, priority, and due date.
- **View tasks** with their status, priority, and due date.
- **Mark tasks as completed**.
- **Remove tasks** by selecting their task number.
- **Prioritize tasks** as High, Medium, or Low.
- **Sort tasks by priority**, with High-priority tasks displayed first.
- **Save and load tasks** using JSON.
- **Interactive menu** for navigating the application.
- **Input validation** for empty descriptions, invalid menu choices, and incorrectly formatted dates.

## Technologies Used

- Python
- JSON for task storage
- Google Colab for development and testing
- Google Drive (optional) for persistent storage across Colab runtime sessions

## Getting Started

### Requirements

- A Google account to use Google Colab
- A web browser
- No third-party Python packages are required for the core application

### Run in Google Colab

1. Open [Google Colab](https://colab.research.google.com/).
2. Create a new notebook and upload or paste the project code into code cells in the correct order.
3. Run the cells that define the functions before running the main application.
4. Run the cell that calls `main()` to open the menu.
5. Follow the menu prompts to add, view, complete, remove, and sort tasks.

### Menu Options

The application menu includes:

1. Add Task
2. View Tasks
3. Mark Task as Completed
4. Remove Task
5. Exit
6. View Tasks Sorted by Priority

The exact menu options depend on the version of the code in the notebook.

## Data Storage

Tasks are stored as JSON records. A task can contain these fields:

```json
{
  "description": "Complete Python internship project",
  "completed": false,
  "priority": "High",
  "due_date": "2026-11-05"
}
```

For persistent storage in Google Colab, mount Google Drive and set the `FILE_NAME` variable to a path inside your Drive, for example:

```python
from google.colab import drive
drive.mount("/content/drive")

import os
PROJECT_FOLDER = "/content/drive/MyDrive/InfozaTech_Internship"
os.makedirs(PROJECT_FOLDER, exist_ok=True)

FILE_NAME = os.path.join(PROJECT_FOLDER, "tasks.json")
```

Run the Google Drive setup before calling `load_tasks()` or `save_tasks()`. Colab's temporary local files may be cleared when a runtime is reset.

## Validation and Testing

Before submitting, test the following:

- Add a task with a valid description, priority, and date.
- Try an empty description.
- Try an invalid date format.
- View tasks and check their status and details.
- Mark a task as completed.
- Remove a task.
- Check that sorting displays High, Medium, then Low priority.
- Save tasks, restart the runtime, and verify that tasks can be loaded from Google Drive.

## Project Structure

A simple GitHub repository structure can be:

```text
InfozaTech-ToDo-List/
├── README.md
├── todo_list.ipynb
└── tasks.json          # Optional sample data only
```

If you include `tasks.json`, use sample data only. Do not upload private or personal information.

## Learning Outcomes

Through this project, I practised:

- Python functions and control flow
- Lists and dictionaries
- User input and validation
- Working with JSON files
- Handling exceptions
- Sorting data using a custom key
- Testing and documenting a small application

## Author

**Harsh Jha**

Created as part of Python internship task practice at InfozaTech.

---

*Note: This README describes the intended features. Before publishing, make sure each listed feature is present and tested in the notebook version you upload.*
