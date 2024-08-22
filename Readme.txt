School Management API
A Node.js API for managing schools, built with Express.js and MySQL. The API allows adding schools and retrieving a list of schools sorted by proximity to a user-specified location.

Features
Add School: Adds a new school with name, address, latitude, and longitude.
List Schools: Fetches and sorts schools by proximity to provided coordinates.
Tech Stack
Node.js & Express.js: Backend framework.
MySQL: Database for storing school data.
Setup
Clone the repo:

bash
Copy code
git clone https://github.com/your-username/school-management-api.git
cd school-management-api
Install dependencies:

bash
Copy code
npm install
Configure environment:

Create a .env file in the root directory with the following:
plaintext
Copy code
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=
DB_NAME=school_management
PORT=3000
Set up MySQL:

Create the school_management database and schools table:
sql
Copy code
CREATE TABLE schools (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    address VARCHAR(255) NOT NULL,
    latitude FLOAT NOT NULL,
    longitude FLOAT NOT NULL
);
Run the server:

bash
Copy code
npm start
API Endpoints
Add School: POST /api/schools/addSchool
List Schools: GET /api/schools/listSchools?latitude={lat}&longitude={lon}