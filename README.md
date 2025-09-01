# todo-api
### This is todo list using `FastAPI`, `Python`, `SQLite` database first create and turn into `PostpreSQL` by `sqlachemy lib` (in progress).

### Todo Model

| Field       | Type     | Description           |
|------------|---------|----------------------|
| id         | Integer | Primary key, auto-increment |
| title      | String  | Title of the todo    |
| description| String  | Optional, todo details |
| completed  | Boolean | True if task is done |

```python
# Example usage
todo = Todo(
    id=1,
    title="Learn FastAPI",
    description="Read docs and create sample app",
    completed=False
)
```

### Flow when client sending a POST

main.py orchestrates the workflow: FastAPI first receives the request and validates the input using the TodoCreate model from schemas.py (Pydantic). It then converts the JSON into a Python object and calls crud.py to store the data in the database. Finally, FastAPI validates the response using the response model and returns it to the client.

### Demo
Test `FastAPI` with GET, POST, PUT, DELETE with swagger UI.

<img width="1528" height="803" alt="image" src="https://github.com/user-attachments/assets/b73d66a3-78f2-436e-9f2d-85ea6c5bde5a" />

Server responed log in command promt.

<img width="1910" height="988" alt="image" src="https://github.com/user-attachments/assets/b334ceb5-5c16-44fe-b88b-6f02220a33bd" />
