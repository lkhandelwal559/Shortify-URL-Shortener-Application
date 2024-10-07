URL Shortener MERN Project



This project is a simple URL Shortener application built using the MERN stack (MongoDB, Express.js, React.js, Node.js). It includes a backend with APIs for user authentication (signup, login) and URL shortening functionality.

Table of Contents
Features
APIs
Prerequisites
Installation
Setting up MongoDB
Running the Project
Project Structure

Features
User Signup and Login: Users can create an account and log in to manage their short URLs.
Home Page: Authenticated users can view their short URLs.
URL Shortening: Shortens long URLs into short, manageable URLs.
APIs
Signup
Method: POST
Endpoint: /api/signup
Description: Registers a new user.
Payload:
{
  "Name": "exampleUser",
  "email": "xyz@abc.com",
  "password": "examplePass"
}
Login
Method: POST
Endpoint: /api/login
Description: Logs in an existing user.
Payload:
{
  "email": "xyz@abc.com",
  "password": "examplePass"
}
Home Page
Method: GET
Endpoint: /api/home
Description: Returns a list of URLs shortened by the logged-in user.
Prerequisites
Node.js (v14 or higher)
npm (Node package manager)
MongoDB (either local or cloud-based like MongoDB Atlas)
Installation
1. Clone the Repository
git clone https://github.com/lkhandelwal559/URL-Shortener/
2. Install Dependencies
npm install
3. Set Up Environment Variables
Create a .env file in the root directory and add the following variables:

PORT=5000
MONGO_URI=mongodb://127.0.0.1:27017/url-shortener
JWT_SECRET=your_jwt_secret
Make sure to replace your_jwt_secret with a secure secret for JWT authentication.

Setting Up MongoDB
1. Download MongoDB
Go to the MongoDB Download Center and download the Community Edition for your operating system. Install it using the MSI installer and make sure to include the MongoDB shell (mongosh) during installation.

2. Create MongoDB Data Directory
MongoDB needs a data directory to store its files. By default, it uses C:\data\db.

Open File Explorer and create the following directories:

C:\data\db
Alternatively, you can create the directory using the Command Prompt:

mkdir C:\data\db
3. Start MongoDB Server
After creating the data directory, start MongoDB by running the following command:

mongod --dbpath "C:\data\db"
This will start the MongoDB server on localhost:27017.

Running the Project
1. Start the Backend Server
After setting up MongoDB and environment variables, you can start the backend server by running:

npm start
The backend should be running at http://localhost:5000.

2. Frontend Setup
The frontend part of the project is built using React. Go into the client directory and install dependencies:

cd client
npm install
To start the React development server:

npm start
The frontend will be running at http://localhost:8001.

Project Structure
├── client                # Frontend (React) application
│   ├── public            # Public directory for frontend assets
│   └── src               # React components and views
├── models                # MongoDB models
│   ├── User.js           # User schema
│   └── Url.js            # URL schema
├── routes                # API routes
│   ├── auth.js           # Authentication routes (signup, login)
│   └── url.js            # URL shortening routes
├── .env                  # Environment variables
├── server.js             # Express server setup
├── package.json          # Backend dependencies and scripts
└── README.md             # Project documentation



