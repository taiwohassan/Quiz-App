# Project README

## Project Overview

This project is a React-based quiz application. It fetches questions from a server, presents them to the user, tracks the user's progress and score, and provides feedback upon completion. The application is structured with various components to handle different stages of the quiz, such as loading, displaying questions, and showing results.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Components](#components)
- [State Management](#state-management)
- [APIs](#apis)
- [License](#license)

## Installation

To get started with this project, follow these steps:

1. **Clone the repository:**
   ```sh
   git clone <git remote add origin https://github.com/taiwohassan/Quiz-App.git>
   ```

2. **Navigate to the project directory:**
   ```sh
   cd <project-directory>
   ```

3. **Install dependencies:**
   ```sh
   npm install
   ```

4. **Start the development server:**
   ```sh
   npm start
   ```

The application should now be running at `http://localhost:3000`.

## Usage

To use the application:

1. Open your browser and navigate to `http://localhost:3000`.
2. The application will automatically fetch questions from the server.
3. Follow the on-screen instructions to start and complete the quiz.

## Components

The application consists of the following components:

- **Header:** Displays the header of the application.
- **Main:** The main container for the quiz content.
- **Loader:** Displays a loading spinner while questions are being fetched.
- **Error:** Displays an error message if there is an issue fetching questions.
- **StartScreen:** Displays the start screen of the quiz.
- **Question:** Displays a single quiz question.
- **NextButton:** Button to proceed to the next question.
- **Progress:** Displays the user's progress through the quiz.
- **FinishedScreen:** Displays the final score and high score at the end of the quiz.
- **Footer:** Contains the footer elements such as the timer.
- **Timer:** Counts down the time remaining for the quiz.

## State Management

The application uses the `useReducer` hook for state management. The state consists of the following properties:

- `questions`: An array of questions fetched from the server.
- `status`: The current status of the application (`loading`, `error`, `ready`, `active`, `finished`).
- `index`: The current question index.
- `answer`: The user's selected answer for the current question.
- `points`: The user's current score.
- `highscore`: The user's highest score.
- `secondsRemaining`: The time remaining for the quiz.

### Reducer Actions

- `dataReceived`: Sets the questions and changes the status to `ready`.
- `dataFailed`: Changes the status to `error`.
- `start`: Starts the quiz and initializes the timer.
- `newAnswer`: Records the user's answer and updates the score.
- `nextQuestion`: Moves to the next question.
- `finished`: Ends the quiz and updates the high score.
- `restart`: Restarts the quiz.
- `tick`: Decrements the timer and finishes the quiz if the time runs out.

## APIs

The application fetches questions from the following endpoint:

- `GET http://localhost:5000/questions`: Fetches an array of questions.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.


