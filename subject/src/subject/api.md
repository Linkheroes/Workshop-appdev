# API Documentation

This documentation describes the API endpoints available for your mobile application. All routes are GET requests and use the base path `/api/`.

## Base URL

```
https://your-api-domain.com/api
```

## Available Endpoints

### Get All Todo Groups

```
GET /api/topics
```

Returns a list of all todo groups.

**Response Example:**

```json
[
    {
        "id": 1,
        "title": "Work Tasks",
        "description": "All work-related todos",
        "created_at": "2024-03-20T10:00:00Z"
    },
    {
        "id": 2,
        "title": "Personal Tasks",
        "description": "Personal todo items",
        "created_at": "2024-03-20T11:00:00Z"
    }
]
```

### Get Specific Todo Group

```
GET /api/topics/:id
```

Returns details for a specific todo group.

**Response Example:**

```json
{
    "id": 1,
    "title": "Work Tasks",
    "description": "All work-related todos",
    "created_at": "2024-03-20T10:00:00Z"
}
```

### Get All Todos in a Group

```
GET /api/topics/:id/todos
```

Returns all todos within a specific group.

**Response Example:**

```json
[
    {
        "id": 1,
        "title": "Complete project documentation",
        "description": "Write technical documentation for the mobile app",
        "status": "pending",
        "created_at": "2024-03-20T10:30:00Z"
    },
    {
        "id": 2,
        "title": "Team meeting",
        "description": "Weekly team sync",
        "status": "completed",
        "created_at": "2024-03-20T11:30:00Z"
    }
]
```

### Get Specific Todo in a Group

```
GET /api/topics/:id/todos/:id
```

Returns details for a specific todo within a group.

**Response Example:**

```json
{
    "id": 1,
    "title": "Complete project documentation",
    "description": "Write technical documentation for the mobile app",
    "status": "pending",
    "created_at": "2024-03-20T10:30:00Z"
}
```

## Data Models

### Todo Group Model

```typescript
{
    id: number;
    title: string;
    description: string;
    created_at: string;
}
```

### Todo Item Model

```typescript
{
    id: number;
    title: string;
    description: string;
    status: "pending" | "completed";
    created_at: string;
}
```

**Note:** All endpoints return JSON data and only support GET requests. Error responses will include appropriate HTTP status codes and error messages.
