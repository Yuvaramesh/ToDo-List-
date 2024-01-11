# ToDo-List-
The user can add their task with or without their due dates

Technologies Used
HTML5: The structure of the web app.
CSS3 with Tailwind CSS: For styling the app beautifully.
JavaScript: To handle the interactive functionality of the app.
Local Storage: To save todos for persistent data across browser sessions.

HTML code represents a basic structure for a Todo List web application. Here's a breakdown of the components:

1. **Document Type Declaration (`<!DOCTYPE html>`) and HTML Tag (`<html>`):**
   - Specifies the document type and language.
   - `data-theme="cupcake"` attribute is used to set the initial theme for the page.

2. **Head Section (`<head>`):**
   - Contains metadata and links to external resources.
   - Meta tags for character set, compatibility, and viewport settings.
   - Links to external CSS files for styling (Tailwind CSS, DaisyUI, and custom `style.css`).
   - Links to external icon libraries (Boxicons).
   - Favicon is set using the `<link rel="icon" href="res/icon-of-a-hand-holding-a-pencil-svgrepo-com.svg">`.
   - Sets the title of the webpage.

3. **Body Section (`<body>`):**
   - Contains the content of the webpage.
   - The content is organized within a `<div class="container">` for styling purposes.
   - **Header Section:**
     - Contains the title "Todo List" and an alert message div.
     - Provides an input section for adding tasks with a text input, date input, and an "Add Task" button.
   - **Todos Filter Section:**
     - Contains a dropdown for filtering tasks by status (All, Pending, Completed).
     - Includes a "Delete All" button.
   - **Table Section (`<table class="table w-full">`):**
     - Represents a table for displaying tasks with columns for Task, Due Date, Status, and Actions.
     - The actual list of tasks will be dynamically populated in the `<tbody class="todos-list-body">` section.
   - **Theme Switcher:**
     - A dropdown for changing the theme, with options "bumblebee" and "luxury".
   - **Script Tags:**
     - Links to JavaScript files (`app.js` and `theme.js`) for defining the functionality of the Todo List and theme switching.

4. **Scripts (`<script>`):**
   - Links to JavaScript files for defining the behavior and functionality of the Todo List and theme switching.

HTML structure provides a foundation for a Todo List application with features like adding tasks, filtering tasks, and changing themes. The dynamic aspects and interactions are likely implemented using JavaScript (as indicated by the script tags). Additionally, the styling is facilitated by external CSS frameworks (Tailwind CSS and DaisyUI) along with a custom `style.css`.

The JavaScript code is part of a Todo List web application. Below is a breakdown of its main components and functionalities:

1. **Variable Declarations:**
   - `task_input`, `date_input`: Selectors for input elements representing the task description and due date.
   - `add_btn`: Selector for the button to add a new task.
   - `todos_list_body`: Selector for the `<tbody>` element where the list of tasks is displayed.
   - `alert_message`: Selector for displaying alert messages.
   - `delete_all_btn`: Selector for the button to delete all tasks.
   - `todos`: An array to store the tasks. It is initialized by parsing the stored tasks from local storage or set to an empty array.

2. **Window Event Listener:**
   - Listens for the `DOMContentLoaded` event to execute a function that shows all existing todos retrieved from local storage and displays a message if there are no tasks.

3. **Function `getRandomId()`:**
   - Generates a random alphanumeric string to be used as a unique identifier for tasks.

4. **Function `addToDo(task_input, date_input)`:**
   - Adds a new task to the `todos` array with properties like `id`, `task`, `dueDate`, `completed`, and `status`.
   - The `id` is generated using `getRandomId()`.
   - Truncates the task description if it exceeds 14 characters.
   - The new task is then pushed to the `todos` array.

5. **Event Listeners:**
   - Listens for keyup events on the task input field, and if the Enter key is pressed and the task is not empty, a new task is added to the list.
   - Listens for a click event on the "Add Task" button, adds a new task to the list, and clears the input fields.

6. **Function `showAllTodos()`:**
   - Clears the HTML content of the todos list and dynamically generates HTML for each task.
   - Displays a message if no tasks are found.

7. **Function `saveToLocalStorage()`:**
   - Saves the current state of the `todos` array to local storage as a JSON string.

8. **Function `showAlertMessage(message, type)`:**
   - Displays an alert message with a specified message and type (success or error).
   - The message is shown for 3 seconds and then hidden.

9. **Functions for Task Operations:**
   - `deleteTodo(id)`: Deletes a task with a specified ID from the `todos` array.
   - `editTodo(id)`: Retrieves a task with a specified ID for editing and updates the UI accordingly.
   - `clearAllTodos()`: Clears all tasks from the `todos` array.
   - `toggleStatus(id)`: Toggles the completion status of a task with a specified ID.

10. **Function `filterTodos(status)`:**
    - Filters tasks based on their completion status (All, Pending, Completed).
    - Calls the `displayTodos` function to update the UI with the filtered tasks.

11. **Function `displayTodos(todosArray)`:**
    - Displays tasks in the UI based on the provided array.
    - Shows a message if no tasks are found.

Overall, this code provides the functionality for managing a simple Todo List, including adding, editing, deleting, and filtering tasks. The tasks are stored in the local storage of the browser for persistence.
