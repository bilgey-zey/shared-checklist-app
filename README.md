# Shared Checklist App

## Project Description
A shared checklist application that allows users to create lists for different purposes, mark items as completed, and collaborate with others.  
The application is intentionally kept minimal and generic, allowing it to be used for trips, shopping, household tasks, or any other shared activities.

## Project Scope
- General-purpose shared checklist
- Focus on simplicity and collaboration
- No calendar or scheduling features
- No notifications
- No categories or priorities

## Core Features
- User accounts (register / login)
- Create and manage checklists
- Add and complete checklist items
- Share checklists with other users
- Offline support
- PWA support

## Technical Requirements
- Client: Web-based PWA
- Server: REST-style backend
- Database: PostgreSQL (cloud-based)
- Authentication: Custom user authentication
- Offline support with synchronization

## Project Planning
- GitHub Issues for task tracking
- Feature-based work items
- Incremental development approach

## Future Improvements
- Calendar support
- Notifications
- Advanced list organization
- UI enhancements


## Feature Map

### User accounts
- Users can register and log in
- Users have their own checklists

### Checklists
- Create a new checklist
- Edit checklist title
- Delete a checklist

### Checklist items
- Add items to a checklist
- Mark items as completed
- Remove items from a checklist

### Sharing
- Share a checklist with another user
- Multiple users can view and modify the same checklist

### Offline & PWA
- View checklists while offline
- Changes sync when back online


Start working on API
## API Design (Scaffold)

GET /api/checklists

Response (example):
```json
[
  {
    "id": 1,
    "title": "Shopping list"
  },
  {
    "id": 2,
    "title": "Trip preparation"
  }
]
POST /api/checklists

Request body (example):

{
  "title": "Weekend tasks"
}
GET /api/checklists/{id}

Response (example):

{
  "id": 1,
  "title": "Shopping list",
  "items": [
    {
      "id": 1,
      "text": "Milk",
      "completed": false
    },
    {
      "id": 2,
      "text": "Bread",
      "completed": true
    }
  ]
}
POST /api/checklists/{id}/items

Request body (example):

{
  "text": "Buy eggs"
}
PATCH /api/checklists/{id}/items/{itemId}

Request body (example):

{
  "completed": true
}


