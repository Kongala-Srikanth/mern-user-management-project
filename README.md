# User Management Dashboard 
## Frontend
## Overview
This project is a **User Management Dashboard** built using **React.js**. It provides a user interface to view, add, edit, and delete user details. The application communicates with a backend API to manage the users.

## Features
- **View Users:** Display a list of users with their details (first name, last name, email, and department).
- **Add User:** Create a new user by submitting a form.
- **Edit User:** Edit the details of an existing user.
- **Delete User:** Remove a user from the system.
- **Error Handling:** Displays error messages for failed operations.
- **Loader:** Displays a loading state while data is being fetched.

## Tech Stack
- **React.js**: Frontend library for building the user interface.
- **React Router**: For routing between different pages (View, Edit, Add).
- **Fetch API**: To interact with the backend API.
- **CSS**: For styling the components.

## API Endpoints
- **GET /users**: Fetch all users.
- **POST /users/add**: Create a new user.
- **PUT /user/{id}**: Update a user by their `id`.
- **DELETE /user/{id}**: Delete a user by their `id`.

## Installation

### Clone the repository:
```bash
git clone <repository_url>
```

### Navigate to the project directory:
```bash
cd <project_directory>
```

### Install the dependencies:
```bash
npm install
```
### Start the development server:
```bash
npm start
```
This will run the application locally at http://localhost:3000.

## Usage
- 1. **View Users:** Upon opening the dashboard, users' information is fetched and displayed.

- 2. **Add User:** Click the "Add User" button to navigate to a form for creating a new user.

- 3. **Edit User:** Click the "Edit" button next to a user's name to edit their details.

- 4. **Delete User:** Click the "Delete" button to remove a user from the system.



<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

# User Management API
## Backend

This is a Node.js application for managing user data using MongoDB. The project provides APIs to add, update, delete, and fetch user details.

## Features

- **Add User**: Create a new user with unique details.
- **Update User**: Modify details of an existing user.
- **Delete User**: Remove a user from the database.
- **Fetch Users**: Retrieve all user details.

## Requirements

- **Node.js**: Ensure you have Node.js installed (version 14 or higher is recommended).
- **MongoDB Atlas**: Set up a MongoDB Atlas cluster and get the connection string.
- **npm**: Node package manager for installing dependencies.
- **dotenv**: Store sensitive information in an `.env` file.

### 1. Clone the repository:
```bash
git clone <your-repository-url>
cd <your-project-directory>
```
### 2. Install dependencies:
```bash
npm install
```
### 3. Create a .env file in the root directory with the following content:
```bash
DB_USER=<your-db-user>
DB_PASSWORD=<your-db-password>
DB_CLUSTER=<your-db-cluster>
DB_NAME=<your-database-name>
```
### 4. Start the server:
```bash
node <file-name>.js
```
Replace <file-name> with the name of your server file.

### 5. The server runs on port 3000.

## API Endpoints
### 1. Add User
- Endpoint: /users
- Method: POST
- Request Body:
```bash
{
  "firstName": "Srikanth",
  "lastName": "Kongala",
  "email": "srikanth.doe@example.com",
  "department": "Engineering"
}
```
- **Response**:
- 201 Created: User added successfully.
- 401 Unauthorized: User already exists.


### 2. Update User
- Endpoint: /user:id
- Method: PUT
- Request Parameters: id (user's unique identifier):
```bash
{
  "firstName": "Srikanth",
  "lastName": "Kumar",
  "email": "srikanth.kumar@example.com",
  "department": "Marketing"
}

```
- **Response**:
- 200 OK: User updated successfully.
- 404 Not Found: User not found.
- 400 Bad Request: No fields provided to update.


### 3. Delete User
- Endpoint: /user:id
- Method: DELETE
- Request Parameters: id (user's unique identifier):

- **Response**:
- 200 OK: User deleted successfully.
- 404 Not Found: User not found.


### 4. Get All User
- Endpoint: /users
- Method: GET

- **Response**:
- 200 OK: List of all users.
- 500 Internal Server Error: Error fetching user details.


## Technologies Used

- Node.js
- Express.js
- MongoDB
- UUID: For generating unique user IDs.
- dotenv: For environment variable management.
- cors: For handling cross-origin requests.

## Running the Project
- 1. Start the server as described in the installation section.
- 2. Use any API testing tool like Postman or cURL to interact with the API.
- 3. Ensure your MongoDB database is configured correctly in the .env file.

