# AI-CHATBOT

This is a MERN stack application.

## Description

This is an AI-powered Chatbot application built with the MERN stack and OpenAI, inspired by ChatGPT.

The chatbot allows users to interact seamlessly while storing each conversation in a database for retrieval and management. Users can access, review, and delete their chat history as needed.

Security is a top priority, with robust measures including JWT authentication, HTTP-only cookies, signed cookies, password encryption, and middleware chains to ensure data integrity and user privacy

## Features

AI-Powered Conversations – Seamlessly interact with the chatbot, powered by OpenAI.

Chat History Management – Every user message is stored in the database, allowing retrieval and deletion as needed.

Secure Authentication – Implements JWT authentication, HTTP-only cookies, and signed cookies for enhanced security.

Data Protection – Utilizes password encryption and middleware chains to safeguard user information.

MERN Stack Architecture – Built with MongoDB, Express.js, React, and Node.js for a scalable and efficient full-stack experience.

User-Friendly Interface – A clean and intuitive UI for effortless chatbot interactions.

## Tech Stack

### Frontend

- React.js
- TypeScript
- Tailwind CSS/ Material UI

### Backend

- Node.js
- Express.js
- TypeScript
- MongoDB &Mongoose ORM
- JWT Authentication

### Setup Instructions

#### Clone the Repository

```sh
git clone https://github.com/Keerthi-Kolan/AI-CHATBOT.git
cd AI CHAT-BOT

```

#### Install Dependencies

##### Backend

```sh
cd backend
npm install

```

##### Frontend

```sh
cd frontend
npm install

```

#### Setup Environment variables

Create a .env file in the backend folder and add:

```env
OPEN_AI_SECRET=your_open_ai_secret
OPEN_AI_ORGANIZATION_ID=your_open_ai__organization_id
MONGODB_URL=your_mongodb_url
JWT_SECRET=your_jwt_secret
COOKIE_SECRET=your_cookie_secret
PORT=5000

```

### API Endpoints

## API Endpoints

### User Routes

- **`GET /api/user/`**  
  Fetch all users.

- **`POST /api/user/signup`**  
  Register a new user.

- **`POST /api/user/login`**  
  Login a user (returns a JWT token).

- **`GET /api/user/auth-status`**  
  Verify if the user is authenticated.  
  **Access**: Protected (JWT required)

- **`GET /api/user/logout`**  
  Logout the user (invalidates the JWT).  
  **Access**: Protected (JWT required)

### Chat Routes

- **`POST /api/chat/new`**  
  Create a new chat using OpenAI’s chat completion.  
  **Access**: Protected (JWT required)

- **`GET /api/chat/all-chats`**  
  Retrieve all the chats for the authenticated user.  
  **Access**: Protected (JWT required)

- **`DELETE /api/chat/delete`**  
  Delete chats for the authenticated user.  
  **Access**: Protected (JWT required)
