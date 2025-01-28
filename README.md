# RESTful API with Go and SQLite

A simple RESTful API built using [Go](https://golang.org/), [Gin](https://github.com/gin-gonic/gin), and [GORM](https://gorm.io/), demonstrating basic CRUD operations for managing tasks. This project highlights Go's capabilities for building scalable, high-performance web applications.

## Features

- Create, read, update, and delete (CRUD) tasks.
- SQLite database integration with GORM ORM.
- Well-structured API endpoints for easy interaction.
- Built with Gin, a lightweight and fast web framework for Go.

## Endpoints

| Method | Endpoint       | Description               |
|--------|----------------|---------------------------|
| GET    | `/tasks`       | Retrieve all tasks        |
| GET    | `/tasks/:id`   | Retrieve a task by ID     |
| POST   | `/tasks`       | Create a new task         |
| PUT    | `/tasks/:id`   | Update an existing task   |
| DELETE | `/tasks/:id`   | Delete a task by ID       |

## Getting Started

### Prerequisites
- [Go](https://golang.org/) (1.19 or later recommended)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/restful-api.git
   cd restful-api

2. Install dependencies:
```
go mod tidy
```

3. Run the application:
```
go run main.go
```

The server will start on http://localhost:8080

## Example usage

### Create a task
```
curl -X POST http://localhost:8080/tasks \
-H "Content-Type: application/json" \
-d '{
  "title": "Learn Go",
  "description": "Study Goroutines and concurrency",
  "completed": false
}'
```

### Retrieve all tasks
```
curl -X GET http://localhost:8080/tasks
```

### Update a task
```curl
curl -X PUT http://localhost:8080/tasks/1 \
-H "Content-Type: application/json" \
-d '{
  "title": "Learn Go",
  "description": "Master Goroutines and channels",
  "completed": true
}'

```

### Delete a task
```curl
curl -X DELETE http://localhost:8080/tasks/1
```

## Project Structure
```
.
├── main.go        # Application entry point
├── go.mod         # Go module file
├── go.sum         # Dependency lock file
└── tasks.db       # SQLite database (auto-created)
```

