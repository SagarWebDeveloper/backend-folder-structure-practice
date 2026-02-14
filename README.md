# Backend Folder Structure Practice

A simple Node.js + Express backend project
focused on clean folder structure and MongoDB connection.

---

## Tech Stack

* Node.js
* Express
* MongoDB Atlas
* Mongoose

---

## Environment Variables (dotenv)

This project uses **dotenv** to manage environment variables securely.

Sensitive information such as:

* MongoDB connection string
* Application port

are stored inside a `.env` file instead of being hard-coded in the source code.

### Why dotenv is used?

* To keep secrets secure
* To avoid pushing sensitive data to GitHub
* To follow good backend development practices

### Example `.env` file:

```
PORT=8000
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net
```

> Note: The `.env` file is added to `.gitignore` and is not pushed to GitHub.

---

## Exit Handling (process.exit)

The application uses **exit handling** to safely stop the server when a critical error occurs.

For example:

* If MongoDB connection fails
* If the server cannot start properly

In such cases, the application logs the error and exits instead of running in an unstable state.

### Why exit handling is important?

* Prevents the app from running without a database connection
* Helps in debugging serious issues
* Improves overall reliability of the backend

---

## Run Locally

Install dependencies:

```
npm install
```

Start the development server:

```
npm run dev
```

---

## Project Flow (Simple)

1. Environment variables are loaded using dotenv
2. MongoDB connection is established
3. If connection fails → application exits
4. If connection succeeds → server starts on the given port
