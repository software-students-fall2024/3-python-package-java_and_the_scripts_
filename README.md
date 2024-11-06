![Python build & test](https://github.com/software-students-fall2024/3-python-package-java_and_the_scripts_/actions/workflows/build.yaml/badge.svg)

# Python Package Exercise
**Funtasks: A Task Generating Package** 

This package was created by generally following the [Packaging Python Projects](https://packaging.python.org/tutorials/packaging-projects/) guide, with the addition of `pipenv` for virtual environment management. 

## Overview
Funtasks is a simple and fun task management package designed to help you add, complete, and randomly select tasks. It includes features for adding tasks with urgency levels, marking tasks as complete, and generating random tasks or daily goals based on your available time. 

## Team Members

[Natalie Ovcarov](https://github.com/nataliovcharov)  
[Jun Li](https://github.com/jljune9li)  
[Daniel Brito](https://github.com/danny031103)  
[Alvaro Martinez](https://github.com/AlvaroMartinezM)

## Link to Our Package on PyPI
[PyPI package Link](https://pypi.org/project/funtasks/)

## Functions Overview

- **add_task(task_name: str, urgency: int) -> str**  
    - Description: Adds a new task to the list with a specified urgency level.  
    - Parameters:
      - `task_name`: The name of the task to add.
      - `urgency`: An integer representing the urgency level (1–5, with 5 being the most urgent).
    - Returns: A confirmation message upon successful addition.
    - Raises: `ValueError` if the task already exists.
    - Example: 
      ```python
      add_task("Do laundry", 3)
      ```

- **complete_task(task_name: str) -> str**  
    - Description: Marks a task as completed.
    - Parameters:
      - `task_name`: The name of the task to complete.
    - Returns: A confirmation message or a message indicating the task doesn't exist.
    - Example: 
      ```python
      complete_task("Do laundry")
      ```

- **random_task() -> str**  
    - Description: Retrieves a random task from the list.
    - Returns: The name of a random task or a message indicating there are no tasks.
    - Example: 
      ```python
      random_task()
      ```

- **random_daily_goal(available_time: int) -> str**  
    - Description: Suggests a task based on the available time.
    - Parameters:
      - `available_time`: Time available in minutes (used to determine task urgency).
    - Returns: A task that fits the time constraint or a message indicating no tasks are suitable.
    - Example: 
      ```python
      random_daily_goal(25)
      ```

## How to Install and Use This Package

### Platform Configuration
- **Windows** users: Use `python` and `pip` commands instead of `python3` and `pip3` where necessary.
  ```bash
  pip install pipenv
  python your_program_filename.py
  ```

- **macOS/Linux** users: Ensure Python 3 is installed and use `python3`.
  ```bash
  pip3 install pipenv
  python3 your_program_filename.py
  ```

1. **Install `pipenv`** (if not already installed):
    ```bash
    pip3 install pipenv
    ```

2. **Install the package**:
    ```bash
    pip3 install funtasks
    ```

3. **Activate the virtual environment**:
    ```bash
    pipenv shell
    ```

4. **Create a Python program file** to import and use the package:
    ```python
    from funtasks.tasks import add_task, complete_task, random_task, random_daily_goal
    add_task("Tell a joke", 2)
    complete_task("Tell a joke")
    print(random_task())
    print(random_daily_goal(25))
    ```

5. **Run the program**:
    ```bash
    python3 your_program_filename.py
    ```

6. **Exit the virtual environment**:
    ```bash
    exit
    ```

### Alternative: Run the Package Directly

1. **Create and activate** a `pipenv` virtual environment.
2. Run the package directly:
    ```bash
    python3 -m funtasks
    ```
3. **Exit the virtual environment**:
    ```bash
    exit
    ```

## How to Run Unit Tests
We've included three unit tests for each function in the `funtasks` package. To run these tests:

1. Install `pytest` in the virtual environment:
    ```bash
    pipenv install pytest
    ```
2. Run the tests from the main project directory:
    ```bash
    python3 -m pytest
    ```
3. Verify all tests pass to ensure correct functionality.

## How to Contribute to Funtasks

### Prerequisites
Make sure you have Python 3.9 or higher installed:
```bash
python3 --version
```

1. **Clone the repository**:
    ```bash
    git clone https://github.com/software-students-fall2024/3-python-package-java_and_the_scripts_.git
    ```

2. **Enter the directory**:
    ```bash
    cd 3-python-package-java_and_the_scripts_
    ```

3. **Set up a virtual environment using `pipenv`**:
    ```bash
    pipenv install --dev
    ```

4. **Activate the virtual environment**:
    ```bash
    pipenv shell
    ```

5. **Modify and run the file**:
    ```bash
    python -m funtasks
    ```

   If you want to run a specific file (like `tasks.py`), use:
    ```bash
    python funtasks/tasks.py
    ```

6. **Run tests**:
    ```bash
    pipenv run pytest
    ```

7. **Build the package**:
    ```bash
    python3 -m build
    ```

8. **Exit the virtual environment**:
    ```bash
    exit
    ```


## Continuous Integration

This project has a continuous integration workflow that builds and runs unit tests automatically with every push to GitHub.