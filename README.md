
# ToDo App

This project is a simple Node.js-based ToDo application developed for the SIT737 Cloud Native Application Development unit.  
It demonstrates how to build a full-stack app using Express, EJS, and Docker, with health checks and restart policies managed through Docker Compose.

---

## Features

- Create, view, and manage to-do items
- EJS-based dynamic views
- RESTful routing with method-override
- Dockerized setup with Docker Compose support
- Health check endpoint for container management

---

## Technologies Used

- Node.js  
- Express.js  
- EJS (Embedded JavaScript templates)  
- Docker  
- Docker Compose

---

## Prerequisites

Ensure the following are installed on your system:

- Node.js: https://nodejs.org/
- npm: https://docs.npmjs.com/downloading-and-installing-node-js-and-npm
- Docker: https://www.docker.com/
- Docker Compose: https://docs.docker.com/compose/install/

---

## Running the App Locally (Without Docker)

1. **Clone the repository**

   git clone https://github.com/your-username/toDo.git  
   cd toDo

2. **Install dependencies**

   npm install

3. **Start the application**

   npm start

4. **Access the app**

   Open your browser and go to:  
   http://localhost:3000/todos

   To verify the health of the app, visit:  
   http://localhost:3000/todos/healthz

---

## Running the App with Docker

1. **Build the Docker image**

   docker build -t todo-app .

2. **Run the Docker container**

   docker run -p 3000:3000 todo-app

3. **Access the app**

   Open your browser and go to:  
   http://localhost:3000

---

## Running the App with Docker Compose

This project includes a docker-compose.yml file for simplified setup and enhanced container behavior.

1. **Start the app using Docker Compose**

   docker-compose up

2. **What this command does**

   - Builds the Docker image
   - Starts the app on port 3000
   - Automatically restarts the app on failure
   - Performs health checks every 30 seconds using the /healthz endpoint

3. **Access the app**

   Open your browser and go to:  
   http://localhost:3000/todos

   Health check endpoint:  
   http://localhost:3000/healthz

---

## Notes

- The app uses method-override to support PUT and DELETE HTTP methods in forms.
- EJS is used as the templating engine, with views stored in the views/ directory.
- CSS files are served statically from the public/css/ directory.
- ToDo-related routes are defined in routes/toDoRoutes.js.
