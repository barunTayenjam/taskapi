# Task Management API

This API manages tasks through various endpoints allowing CRUD operations and sorting based on different parameters.

## Endpoints:

### `GET /tasks/`
- **Description:** Retrieve all tasks.
- **Response:** Returns a list of all tasks.

### `GET /tasks/:id`
- **Description:** Retrieve a specific task by ID.
- **Parameters:** `:id` - ID of the task to be retrieved.
- **Response:** Returns the task if found, else returns a 'Not Found' error.

### `POST /tasks/`
- **Description:** Create a new task.
- **Request Body:** JSON object with `task_title` and `task_description`.
- **Response:** Creates and returns the new task if details are valid, else returns an 'Invalid Details' error.

### `PUT /tasks/:id`
- **Description:** Update a specific task by ID.
- **Parameters:** `:id` - ID of the task to be updated.
- **Request Body:** JSON object with optional fields: `task_title`, `task_description`, `task_status`.
- **Response:** Updates and returns the task if found, else returns a 'Not Found' error.

### `DELETE /tasks/:id`
- **Description:** Delete a specific task by ID.
- **Parameters:** `:id` - ID of the task to be deleted.
- **Response:** Deletes the task if found and returns a success message with the updated task list, else returns a 'Not Found' error.

### `GET /tasks/sort/:type/:order`
- **Description:** Sort tasks based on parameters.
- **Parameters:** 
  - `:type` - Sorting parameter (task_title, created, status).
  - `:order` - Sorting order (asc, desc).
- **Response:** Sorts tasks by the specified parameter in the specified order and returns the sorted list.

### Sorting Options:
- `task_title`: Sort tasks by title.
- `created`: Sort tasks by creation date.
- `status`: Sort tasks by status.
