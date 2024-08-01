## Authorization Service


### Overview
A unified server for user registration, authentication, and task management. The server issues JWT tokens for secure access to task operations.

### Endpoints

#### User Management
Register: POST /api/v1/auth/register

Authenticate: POST /api/v1/auth/authenticate

#### Task Management

Get All Tasks: GET /api/v1/tasks

Get Task by ID: GET /api/v1/tasks/{id}

Create Task: POST /api/v1/tasks

Update Task: PUT /api/v1/tasks/{id}

Delete Task: DELETE /api/v1/tasks/{id}

### Usage
Register a User:


``` 
curl -X POST http://localhost:8080/api/v1/auth/register -H "Content-Type: application/json" -d '{"username":"testuser","password":"testpass"}'
```
Authenticate:

``` 
curl -X POST http://localhost:8080/api/v1/auth/authenticate -H "Content-Type: application/json" -d '{"username":"testuser","password":"testpass"}'
``` 

Access Tasks: 

Use the received JWT token as Bearer token for task operations.
