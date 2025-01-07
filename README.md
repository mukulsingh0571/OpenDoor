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
    cd api
    npm install

    cd ../client
    npm install
```

3. **ICreate a .env file in the api directory with the following environment variables:**

