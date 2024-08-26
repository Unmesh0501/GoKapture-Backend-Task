x`# Task Management Application (GoKapture Backend Assignment)

## Documentation -

**Postman Documentation:** https://documenter.getpostman.com/view/23652247/2sA3s7hnuw

## Features

- **Create, Read, Update, Delete (CRUD)** tasks
- **User Authentication** and authorization
- **Role-Based Access Control**
- **Search and Filter** tasks by status, priority, and due date, title and description
- **Pagination** support for task lists

## Tech Stack

- **Backend**: Node.js with TypeScript using Express.js framework for building the RESTful API.
- **Database**: PostgreSQL as the relational database for storing user and task data.
- **ORM**: Prisma ORM for managing database operations with type safety and migrations.
- **Authentication**: JWT for secure user authentication and authorization.
- **Validation**: Zod for request data validation

## Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/Unmesh0501/GoKapture-Backend-Task.git
   cd GoKapture-Backend-Task
   ```

2. **Installing the dependencies**:

   ```bash
   npm install
   ```

3. **Starting the Application**:
   ```bash
   npm run start:dev
   ```

#### Note: You need to add your PostgreSQL database URL in the .env file after setting up prisma

prisma docs - https://www.prisma.io/docs/getting-started/setup-prisma/start-from-scratch/relational-databases-typescript-postgresql

## Run using Docker:

### Building the image:
 ```bash
   docker build -t name .
   ```

### Running the container:
 ```bash
    docker run -p 3000:3000 name
   ```

## API Endpoints -

### Authentication Endpoints

**User Registration:** POST /api/user/register

**User Login**: POST /api/user/login

### Task Endpoints

**Get all tasks of a user:** GET /api/tasks/all

**Create a new task**: POST /api/tasks/create

**Get All Created Tasks With Pagination**: GET /api/tasks/bulk

**Update a task:** PATCH /api/tasks/update

**Delete a task:** DELETE /api/tasks/delete

**Search tasks:** GET /api/tasks/search?query=:searchTerm

query can be title or description

**Filter tasks:** GET /api/tasks/filter?status=:status&priority=:priority

status = ["todo", "in_progress", "done"]

priority = ["low", "medium", "high"]
