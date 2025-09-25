# FastAPI-To-Do-List-
A simple FastAPI-based Todo API with CRUD functionality. Supports priorities (High, Medium, Low), query parameters, and Pydantic validation. Perfect for learning REST API development with FastAPI.
## 🚀 Features
- **CRUD Operations**
  - `GET /todos` → Fetch all todos (with optional `first_n` query param).
  - `GET /todos/{id}` → Fetch a todo by ID.
  - `POST /todos` → Create a new todo.
  - `PUT /todos/{id}` → Update an existing todo.
  - `DELETE /todos/{id}` → Delete a todo by ID.
- **Priority Levels**: HIGH, MEDIUM, LOW (using `IntEnum`).
- **Validation with Pydantic**:
  - Minimum/maximum lengths for todo names.
  - Optional partial updates with `TodoUpdate`.
- **In-memory storage** (list-based for simplicity).
API EndPoints:
  - GET ALL TODOS:
      GET /todos
  - GET A SINGLE TODO:
      GET /todos/{todo_id}
  - CREATE A NEW TODO:
      POST /todos
    Content-Type: application/json
  {
    "todo_name": "Read book",
    "todo_description": "Finish reading chapter 5",
    "priority": 2
  }  
  - UPDATE A TODO:
      PUT /todos/{todo_id}
  Content-Type: application/json
  {
    "todo_name": "Updated name",
    "priority": 1
  }
  - DELETE A TODO:
      DELETE /todos/{todo_id}    
