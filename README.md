#OnlineQuizApplication
A fun, interactive, and fully responsive Online Quiz Application built using HTML, CSS, JavaScript (Frontend) and Node.js, Express.js, MongoDB (Backend).

It allows users to create an account, attempt quizzes, track progress, and view leaderboard rankings.
This project is designed to make learning engaging and testing knowledge lively through a colorful interface and smooth animations.

📋 Table of Contents

About

Features

Project Structure

Installation & Usage

Tech Stack

Validation Rules

Testing

Contributing

License

🧾 About

The Online Quiz Application is a web-based project developed to test users’ knowledge in Computer Science through a set of 10 multiple-choice questions.
Each question carries equal marks and comes with a 60-second timer, enhancing focus and excitement.

This project aims to provide an interactive platform for students or learners to participate in quiz competitions, analyze their scores, and compare their performance with others through a Leaderboard.

The design uses bright colors, modern animations, and a user-friendly layout that ensures smooth navigation between the login, quiz, and result pages.

It supports both frontend-only (Local Storage) functionality and backend integration (MongoDB) for real-time data storage.

✨ Features

User Authentication – Create account and Login pages using Local Storage.

Welcome Page with Rules – Displays quiz rules, instructions, and a “Start Quiz” button.

Timed Quiz – Each question has a 60-second countdown timer.

Progress Bar – Visual progress indicator above the questions.

Leaderboard – Displays top 5 scores dynamically fetched from MongoDB or stored locally.

Review Answers – Shows only the wrongly answered questions with correct solutions.

Responsive & Animated UI – Modern gradient theme with smooth transitions and mobile-friendly design.

Local Storage Integration – Saves user session, quiz progress, and offline scores.

Backend APIs – RESTful API endpoints for questions, submissions, and leaderboard.

Error Handling & Validation – Input validation for login/signup and graceful error handling for API failures.

🧩 Project Structure
OnlineQuizApplication/
│
├── frontend/
│   ├── index.html          # Main HTML file with embedded CSS and JS
│   └── assets/             # (Optional) images, icons, etc.
│
├── backend/
│   ├── server.js           # Main Express server
│   ├── models.js           # Mongoose schema for Questions
│   ├── userModel.js        # (Optional) User schema
│   ├── package.json        # Backend dependencies and scripts
│   └── seed.js             # (Optional) Script to insert quiz questions
│
├── README.md               # Project documentation
└── phase5_report.docx      # College submission document

⚙️ Installation & Usage
🔧 Prerequisites

Node.js (v16+)

MongoDB or MongoDB Compass

Any modern browser (Chrome / Edge / Firefox)

🧰 Steps to Run Locally

Clone the Repository

git clone https://github.com/your-username/online-quiz-application.git
cd online-quiz-application


Setup Backend

cd backend
npm install
node server.js


The server runs at: http://localhost:5000

Start MongoDB

Open MongoDB Compass or terminal.

Connect to mongodb://127.0.0.1:27017.

Create a database named quizapp.

Create a collection named questions.

Insert your 10 quiz questions manually or run seed.js.

Run Frontend

Open frontend/index.html in your browser

or use VS Code Live Server Extension

Start Playing!

Create an account → Read rules → Start quiz → Finish → View leaderboard.

💻 Tech Stack

Frontend:

HTML5

CSS3 (Animations & Responsive Design)

JavaScript (Vanilla)

Backend:

Node.js

Express.js

Database:

MongoDB (Mongoose ORM)

Tools & Libraries:

CORS

Nodemon

MongoDB Compass

🧮 Validation Rules

Frontend Validation:

User must enter valid email format during signup.

Password field cannot be blank.

Name must contain at least 3 characters.

Timer automatically submits unanswered questions after 60 seconds.

Backend Validation:

Score submission only allowed if name, email, and score are provided.

Prevents duplicate user creation — updates score if higher than previous.

Database schema ensures question format correctness.

🧪 Testing

Manual Testing:

Verified all input fields for correct/incorrect inputs.

Checked timer countdown accuracy for each question.

Tested backend routes using Postman:

/api/questions → Returns 10 questions

/api/submit → Saves score and returns success message

/api/leaderboard → Returns top 5 scores

Cross-Browser Testing:

Works on Chrome, Edge, and Firefox.

Responsive design validated on desktop and mobile viewports.

Error Handling:

Displays alert for invalid login/signup data.

Automatically switches to local fallback questions if backend unavailable.

🤝 Contributing

Contributions are welcome!
If you’d like to improve UI/UX, add new features, or enhance backend functionality, follow these steps:

Fork the repository.

Create a new branch:

git checkout -b feature-new


Make your changes and commit:

git commit -m "Add new feature"


Push to your branch:

git push origin feature-new


Submit a pull request.

📜 License
This project is licensed under the MIT License.

You are free to use, modify, and distribute this software for personal and educational purposes, provided that proper credit is given.

This project is licensed under the MIT License.

You are free to use, modify, and distribute this software for personal and educational purposes, provided that proper credit is given.
