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
### `app.js`:

1. **Variables:**
   - Selectors for inputs and buttons.
   - Array for storing tasks.

2. **DOMContentLoaded:**
   - Shows existing tasks on page load.

3. **getRandomId():**
   - Generates unique task IDs.

4. **addToDo():**
   - Adds tasks to the array with properties.
   - Truncates long task descriptions.

5. **Event Listeners:**
   - Handles key and button clicks.

6. **showAllTodos():**
   - Dynamically generates HTML for tasks.
   - Displays a message if no tasks.

7. **saveToLocalStorage():**
   - Stores tasks in local storage.

8. **showAlertMessage():**
   - Displays alert messages.

9. **Task Operations Functions:**
   - deleteTodo, editTodo, clearAllTodos, toggleStatus.

10. **filterTodos():**
    - Filters tasks based on status.

11. **displayTodos():**
    - Displays tasks in the UI.

### `theme.js`:

1. **Variables:**
   - Selectors for theme options.

2. **DOMContentLoaded:**
   - Sets the theme from local storage.

3. **Event Listeners on Theme Options:**
   - Handles theme clicks.

4. **saveTheme():**
   - Stores selected theme in local storage.

5. **getTheme():**
   - Retrieves current theme from local storage.
Overall, this code provides the functionality for managing a simple Todo List, including adding, editing, deleting, and filtering tasks. The tasks are stored in the local storage of the browser for persistence.
