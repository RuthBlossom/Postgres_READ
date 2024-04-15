# Quiz Game with PostgreSQL Database

This Node.js application is a quiz game built with Express.js and PostgreSQL. It allows users to play a quiz game where they have to guess the country based on its flag. The application fetches quiz data from a PostgreSQL database, presents questions to users, accepts their answers, and provides feedback on correctness.

## Prerequisites
- Node.js installed on your machine.
- PostgreSQL database server installed and running.

## Installation
1. Clone or download this repository.
2. Navigate to the project directory in your terminal.
3. Install dependencies:
    ```bash
    npm install
    ```
4. Set up your PostgreSQL database and import quiz data. The schema for the `flags` table should have at least the following columns: `id`, `name`, and `flag_image`.
5. Configure the database connection in `app.js` with your PostgreSQL credentials.

## Usage
1. Start the application:
    ```bash
    npm start
    ```
2. Open your web browser and navigate to `http://localhost:3000`.
3. Answer the quiz questions by typing the name of the country.
4. Receive feedback on the correctness of your answers and see your total score.

## File Structure
- **app.js**: Main application file containing the Express.js server setup and route definitions.
- **public/**: Directory containing static assets like CSS and client-side JavaScript.
- **views/index.ejs**: EJS template file for rendering the quiz game interface.
- **package.json**: File containing project metadata and dependencies.

## Database Schema
- Ensure your PostgreSQL database has a table named `flags` with columns `id`, `name`, and `flag_image` to store quiz data.

## Dependencies
- **express**: Web framework for Node.js.
- **body-parser**: Middleware for parsing HTTP request bodies.
- **pg**: PostgreSQL client for Node.js.
- **ejs**: Templating engine for rendering HTML templates.

## Routes
- **GET "/":** Renders the index page with the current quiz question.
- **POST "/submit":** Handles form submissions for answering quiz questions.

## Error Handling
- Error handling is implemented for database queries and other asynchronous operations.

## Disclaimer
This application is for educational purposes only.
