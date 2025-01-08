# OpenDoor - Real Estate Website

OpenDoor is a full-stack real estate platform built using the MERN stack (MongoDB, Express.js, React.js, Node.js). The platform allows users to search, view, and apply for available properties while providing admin features to manage property listings efficiently.

## Features

- **User Authentication**: Secure login, sign-up, and JWT-based authentication for users and admins.
- **Property Listings**: Browse, search, and filter property listings based on various criteria (location, price, etc.).
- **Admin Panel**: Manage, add, update, and remove property listings.
- **Real-Time Communication**: Chat functionality using WebSockets (Socket.io).
- **Responsive Design**: Optimized for both desktop and mobile devices.
- **Secure Deployment**: Deployed using AWS EC2 with NGINX as a reverse proxy.

## Tech Stack

- **Frontend**: React.js, Vite, Redux, TailwindCSS
- **Backend**: Node.js, Express.js
- **Database**: MongoDB (MongoDB Atlas for cloud hosting)
- **Real-time Communication**: Socket.io
- **Authentication**: JSON Web Tokens (JWT)
- **State Management**: Redux
- **Hosting**: AWS EC2, NGINX

## Prerequisites

Before you begin, ensure you have the following installed:

- [Node.js](https://nodejs.org/) (v16 or higher)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
- [MongoDB](https://www.mongodb.com/) (or MongoDB Atlas for cloud database)
- [Git](https://git-scm.com/)
- [PM2](https://pm2.keymetrics.io/) (for managing backend server)
- [Nginx](https://www.nginx.com/) (if using reverse proxy)

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/OpenDoor.git
   cd OpenDoor
   ```
2. **Install dependencies for both the frontend and backend:**

    ```bash
        DATABASE_URL="mongodb+srv://username:password@cluster.mongodb.net/OpenDoor?retryWrites=true&w=majority"
        JWT_SECRET_KEY="your-secret-key"
        CLIENT_URL="http://localhost:5173"
    ```

3. **Create a .env file in the api directory with the following environment variables:**

    ```bash
        cd api
        npm install

        cd ../client
        npm install
    ```

4. **Build the frontend for production:**

    ```bash
        cd client
        npm run build
    ```

5. **Start the backend server:**

    - Using PM2 (recommended for production):

        ```bash
            cd api
            pm2 start server.js --name backend
        ```
    - For local development:

        ```bash
            cd api
            npm start
        ```

6. **Serve the frontend using a static server or configure NGINX to serve it:**

    - For local hosting:

        ```bash
        cd client
        npm install -g serve
        serve -s dist
        ```

7. **Configure NGINX as a reverse proxy to handle requests and forward them to the backend:** 

    ```bash
        cd api
        npm install

        cd ../client
        npm install
    ```

## Project Structure

        OpenDoor/
        |
        |-- api/                  # Backend API code (Node.js, Express)
        |   |-- controllers/      # API logic and business logic
        |   |-- models/           # Mongoose models
        |   |-- routes/           # API route definitions
        |   |-- .env              # Environment variables
        |   |-- server.js         # Main entry point for the backend server
        |
        |-- client/               # Frontend code (React.js)
        |   |-- src/              # React components and pages
        |   |-- dist/             # Build directory for production
        |   |-- package.json      # Frontend dependencies and scripts
        |   |-- vite.config.js    # Vite configuration file
        |
        |-- socket/               # WebSocket (Socket.io) configuration
        |   |-- server.js         # WebSocket server

## Scripts

### Backend

- **`npm run dev`**: Start the backend server in development mode.
- **`npm start`**: Start the backend server in production mode using PM2.

### Frontend

- **`npm start`**: Start the frontend development server.
- **`npm run build`**: Build the frontend for production.

## Deployment

For deploying to AWS EC2:

1. Set up an EC2 instance and SSH into it.
2. Clone the repository and follow the **Installation** steps.
3. Set up **PM2** to manage the backend process.
4. Configure **NGINX** as a reverse proxy to route requests to the frontend and backend.
5. Open your application on the browser.

## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgements

- [MongoDB](https://www.mongodb.com/)
- [React](https://reactjs.org/)
- [Node.js](https://nodejs.org/)
- [Express.js](https://expressjs.com/)
- [Socket.io](https://socket.io/)
- [Vite](https://vitejs.dev/)
- [PM2](https://pm2.keymetrics.io/)

Happy Coding😊