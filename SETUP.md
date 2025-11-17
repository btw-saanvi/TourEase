# Setup & Installation Guide for TourEase

This guide will help you set up and run TourEase locally without errors.

## 1. Clone the Repository

git clone https://github.com/Suhani1234-5/TourEase.git
cd TourEase


## 2. Install Dependencies


npm install


For frontend (if using Vite/React in `client/` folder):


cd client
npm install
cd ..


## 3. Install Required Tools


npm install -g nodemon
npm install -g vite


## 4. Create Environment Variables

Create a `.env` file in the root folder:


MONGODB_URI=your-mongodb-uri
PORT=3000


## 5. Run the Project

### Backend:


npm start


Or with nodemon:


nodemon app.js


### Frontend:


cd client
npm run dev


## 6. Common Errors & Fixes

* MongoDB connection error: Check `MONGODB_URI` and ensure MongoDB is running.
* Port already in use: Change `PORT` in `.env` or stop other processes.
* Dependencies missing: Run `npm install` in backend and frontend.
* Nodemon not found: Install globally `npm install -g nodemon`.
