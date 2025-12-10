# Task Manager Application

TrackIt - A full-stack task management application

## Features

- User authentication (Register/Login)
- Create, read, update, and delete tasks
- Filter tasks by status (All, Completed, Pending, Overdue)
- Task priority levels (Low, Medium, High)
- Due date tracking
- Task completion statistics
- Responsive design

## Tech Stack

**Frontend:**
- Next.js 14
- React
- TypeScript
- Tailwind CSS
- Recharts (for data visualization)

**Backend:**
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT Authentication
- Bcrypt for password hashing

## Prerequisites

Before running this application, make sure you have the following installed:
- Node.js (v18 or higher)
- npm or yarn
- MongoDB Atlas account (or local MongoDB)

## Installation & Setup

### 1. Clone the Repository

```bash
git clone <your-repo-url>
cd TrackIt-main
```

### 2. Backend Setup

```bash
# Navigate to backend folder
cd backend

# Install dependencies
npm install

# Create .env file in the backend folder
```

Add these environment variables to your `backend/.env` file:

```env
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_super_secret_jwt_key
CLIENT_URL=http://localhost:3000
PORT=8000
```

**To get your MongoDB URI:**
1. Create an account at [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
2. Create a new cluster
3. Go to Database → Connect → Connect your application
4. Copy the connection string and replace `<password>` with your database password

### 3. Frontend Setup

```bash
# Navigate to client folder (from root)
cd client

# Install dependencies
npm install
```

## Running the Application

You need to run both backend and frontend servers:

**Terminal 1 - Backend:**
```bash
cd backend
npm start
# or
npm run dev
```

The backend will run on `http://localhost:8000`

**Terminal 2 - Frontend:**
```bash
cd client
npm run dev
```

The frontend will run on `http://localhost:3000`

## Usage

1. Open your browser and go to `http://localhost:3000`
2. Register a new account or login
3. Start creating and managing your tasks!

## Project Structure

```
TrackIt-main/
├── backend/
│   ├── src/
│   │   ├── controllers/
│   │   ├── models/
│   │   ├── routes/
│   │   └── middleware/
│   ├── .env
│   └── package.json
├── client/
│   ├── app/
│   │   ├── Components/
│   │   ├── login/
│   │   ├── register/
│   │   └── layout.tsx
│   ├── context/
│   ├── providers/
│   └── package.json
└── README.md
```

## Environment Variables

### Backend (.env)
- `MONGO_URI` - MongoDB connection string
- `JWT_SECRET` - Secret key for JWT token generation
- `CLIENT_URL` - Frontend URL (for CORS)
- `PORT` - Backend server port (default: 8000)

## Troubleshooting

**Backend not connecting to MongoDB:**
- Check your MongoDB connection string
- Make sure your IP is whitelisted in MongoDB Atlas
- Verify your database username and password

**Frontend can't connect to backend:**
- Ensure backend is running on port 8000
- Check that `CLIENT_URL` in backend .env matches your frontend URL
- Verify CORS settings in backend

**Tasks not loading:**
- Check browser console for errors
- Verify the API endpoints in `taskContext.js` use `http://localhost:8000/api/v1`

## License

This project is for educational purposes.
