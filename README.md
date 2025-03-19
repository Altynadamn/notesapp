# MERN Notes App

## Overview
A full-stack note-taking application built using the MERN (MongoDB, Express.js, React.js, Node.js) stack. Users can create, edit, delete, and organize their notes with authentication and a user-friendly interface.

## Features
- User authentication (JWT-based login/register)
- CRUD operations for notes
- Rich text editor for better note formatting
- Categorization and search functionality
- Dark mode support
- Protected routes for authenticated users
- Responsive design

## Tech Stack
- **Frontend:** React.js, React Router, Axios, TailwindCSS (or any preferred CSS framework)
- **Backend:** Node.js, Express.js, MongoDB (Mongoose ODM)
- **Authentication:** JSON Web Tokens (JWT), bcrypt for password hashing
- **Storage:** MongoDB for storing notes

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/Altynadamn/mern-notes-app.git
   cd mern-notes-app
   ```
2. Install dependencies for both frontend and backend:
   ```sh
   cd client
   npm install
   cd ../server
   npm install
   ```
3. Set up environment variables:
   - Create a `.env` file in the `server` directory with the following:
     ```env
     MONGO_URI=your_mongodb_connection_string
     JWT_SECRET=your_secret_key
     ```
4. Start the backend server:
   ```sh
   cd server
   npm start
   ```
5. Start the frontend:
   ```sh
   cd client
   npm start
   ```

## API Endpoints
### Authentication
- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - User login
- `GET /api/auth/user` - Get current user data

### Notes
- `GET /api/notes` - Get all notes
- `GET /api/notes/:id` - Get a single note by ID
- `POST /api/notes` - Create a new note (authenticated)
- `PUT /api/notes/:id` - Update a note (authenticated)
- `DELETE /api/notes/:id` - Delete a note (authenticated)

## Folder Structure
```
mern-notes-app/
├── frontend/    
│   ├── src/
│   ├── public/
│   ├── index.html
│   ├── postcss.config.js
│   ├── tailwind.config.js
│   ├── vite.config.js
│   ├── package-lock.json
│   └── package.json
├── backend/  
│   ├── models/
│   ├── index.js
│   ├── utilities.js
│   ├── package-lock.json
│   └── package.json
└── README.md
```

## Contributing
1. Fork the repository.
2. Create a new branch: `git checkout -b feature-branch`.
3. Commit changes: `git commit -m "Add new feature"`.
4. Push the branch: `git push origin feature-branch`.
5. Submit a pull request.

## License
This project is licensed under the MIT License.

