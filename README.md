# Cinema System

# Getting Started
To run the application, ensure you have Java installed on your system. You can compile and run the project using any Java IDE or the command line.

### PostgreSQL:
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    username VARCHAR(50) NOT NULL,
    password VARCHAR(50) NOT NULL
);

CREATE TABLE movies (
id SERIAL PRIMARY KEY,
title VARCHAR(255) NOT NULL,
description TEXT
); 

CREATE TABLE tickets (
id SERIAL PRIMARY KEY,
userId INT NOT NULL REFERENCES users(id),
movieId INT NOT NULL REFERENCES movies(id)
);
