

```markdown
# SQLTest

## Overview
SQLTest is a Node.js application that provides a RESTful API to interact with a SQL Server database. This application uses Express.js for handling HTTP requests and `mssql` for database interactions. The app also utilizes environment variables for configuration management.
Frontend (index.html)
HTML Structure: Defines the structure of the webpage, including a table to display the list of movies.
Bootstrap: A CSS framework used to style the webpage and make it responsive.
JavaScript (movies.js): A script to interact with the backend API to fetch and display movie data in the table.
Backend (server.js)
Express.js: Handles HTTP requests and serves API endpoints for the frontend to interact with the database.
SQL Server: Stores the movie data and is accessed by the backend using SQL queries.'

Complete Tech Stack
Frontend: HTML, CSS (Bootstrap), JavaScript
Backend: Node.js, Express.js
Database: Azure SQL Server
Environment Configuration: dotenv
Middleware: CORS, express.json()
Interaction Flow
The user opens index.html in a browser.
The JavaScript in movies.js makes an HTTP GET request to the backend API (e.g., /movies endpoint) to fetch the list of movies.
The backend receives the request, retrieves the movie data from the SQL Server database, and sends it back as a JSON response.
The frontend receives the JSON data and dynamically updates the table with the movie information.
## Features
- Connect to a SQL Server database.
- Retrieve all movies.
- Retrieve movies by title.
- Retrieve movies by year.
- Add a new movie.

## Prerequisites
- Node.js (>=14.x.x)
- NPM (>=6.x.x)
- SQL Server database

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/sqltest.git
   cd sqltest
   ```

2. Install dependencies:
   ```sh
   npm install
   ```

3. Create a `.env` file in the root directory and add your database configuration:
   ```plaintext
   DB_USER=myusername
   DB_PASSWORD=Yearup2024!
   DB_SERVER=yearup.database.windows.net
   DB_DATABASE=yearupdemo
   ```

4. Start the server:
   ```sh
   npm start
   ```
   The API will be running at `http://localhost:3000`.

## API Endpoints

### Get all movies
- **URL:** `/movies`
- **Method:** `GET`
- **Description:** Retrieves a list of all movies.
- **Response:**
  ```json
  [
    {
      "id": 1,
      "title": "Movie Title",
      "director": "Director Name",
      "year": 2020,
      "length_minutes": 120
    }
  ]
  ```

### Get movies by title
- **URL:** `/movies/title/:title`
- **Method:** `GET`
- **Description:** Retrieves movies that match the given title.
- **Response:**
  ```json
  [
    {
      "id": 1,
      "title": "Matching Movie Title",
      "director": "Director Name",
      "year": 2020,
      "length_minutes": 120
    }
  ]
  ```

### Get movies by year
- **URL:** `/movies/year/:year`
- **Method:** `GET`
- **Description:** Retrieves movies released in the specified year.
- **Response:**
  ```json
  [
    {
      "id": 1,
      "title": "Movie Title",
      "director": "Director Name",
      "year": 2020,
      "length_minutes": 120
    }
  ]
  ```

### Add a new movie
- **URL:** `/movies`
- **Method:** `POST`
- **Description:** Adds a new movie to the database.
- **Request Body:**
  ```json
  {
    "title": "New Movie",
    "director": "Director Name",
    "year": 2020,
    "length_minutes": 120
  }
  ```
- **Response:**
  ```json
  {
    "message": "Movie added successfully"
  }
  ```

## License
This project is licensed under the ISC License - see the LICENSE file for details.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## Acknowledgements
- Express.js
- mssql
- dotenv
```

This revision includes proper code block closures, organized section titles, and improved formatting for readability.