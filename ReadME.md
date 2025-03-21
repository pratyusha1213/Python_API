# Travel API

This is a simple REST API built using Flask and SQLAlchemy that manages travel destinations. It allows users to perform CRUD (Create, Read, Update, Delete) operations on a list of travel destinations, including their associated countries and ratings.

## Table of Contents

1. [Project Setup](#project-setup)
2. [API Endpoints](#api-endpoints)
3. [Technologies Used](#technologies-used)
4. [Running the Project](#running-the-project)
5. [License](#license)

## Project Setup

### Prerequisites

Before running the project, ensure that you have the following installed

- Python 3.x
- pip (Python package installer)

### Installing Dependencies

To install the required dependencies, run the following command

```bash
pip install -r requirements.txt
```

This will install Flask, Flask-SQLAlchemy, and other necessary libraries.

### Database Setup

This project uses SQLite for its database. The database is automatically created when the application starts, and a `travel.db` file will be generated in the project directory.

## API Endpoints

### 1. Home Route

- URL ``
- Method `GET`
- Description Returns a welcome message.

Response Example

```json
{
  message Welcome to Travel API
}
```

### 2. Get All Destinations

- URL `destinations`
- Method `GET`
- Description Fetches a list of all destinations.

Response Example

```json
[
  {
    id 1,
    destination Paris,
    country France,
    rating 4.8
  },
  {
    id 2,
    destination Tokyo,
    country Japan,
    rating 4.7
  }
]
```

### 3. Get a Single Destination

- URL `destinationsdestination_id`
- Method `GET`
- Description Fetches a destination by its ID.

Response Example

```json
{
  id 1,
  destination Paris,
  country France,
  rating 4.8
}
```

If the destination is not found, the response will be

```json
{
  error Destination not found!
}
```

### 4. Add a New Destination

- URL `destinations`
- Method `POST`
- Description Adds a new destination to the database.

Request Body Example

```json
{
  destination Barcelona,
  country Spain,
  rating 4.6
}
```

Response Example

```json
{
  id 3,
  destination Barcelona,
  country Spain,
  rating 4.6
}
```

### 5. Update an Existing Destination

- URL `destinationsdestination_id`
- Method `PUT`
- Description Updates an existing destination by its ID.

Request Body Example

```json
{
  destination Barcelona,
  country Spain,
  rating 4.9
}
```

Response Example

```json
{
  id 3,
  destination Barcelona,
  country Spain,
  rating 4.9
}
```

If the destination is not found, the response will be

```json
{
  error Destination not found!
}
```

### 6. Delete a Destination

- URL `destinationsdestination_id`
- Method `DELETE`
- Description Deletes a destination by its ID.

Response Example

```json
{
  message destination was deleted!
}
```

If the destination is not found, the response will be

```json
{
  error Destination not found!
}
```

## Technologies Used

- Flask A lightweight web framework for building web applications and APIs.
- Flask-SQLAlchemy A Flask extension that adds support for SQLAlchemy, an ORM (Object Relational Mapper) for managing the database.
- SQLite A lightweight database engine used for storing destination data.

## Running the Project

To run the project, execute the following command

```bash
python app.py
```

This will start the Flask development server. You can access the API at `http127.0.0.15000` in your browser or any API testing tool like Postman.

