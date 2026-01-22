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

### Get all checklists

**GET** `/api/checklists`

Returns a list of all checklists available to the user.

**Response (example):**
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


### Create a new checklist

**POST** `/api/checklists`

Creates a new checklist owned by the user.

**Request body (example):**
```json
{
  "title": "Weekend tasks"
}


### Get a single checklist

**GET** `/api/checklists/{id}`

Returns one specific checklist with its items.

**Response (example):**
```json
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

### Add item to a checklist

**POST** `/api/checklists/{id}/items`

Adds a new item to a specific checklist.

**Request body (example):**
```json
{
  "text": "Buy eggs"
}

### Update item completion status

**PATCH** `/api/checklists/{id}/items/{itemId}`

Updates the completion status of a specific checklist item.

**Request body (example):**
```json
{
  "completed": true
}



