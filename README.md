
# User Registration API

This project is a user registration system built with Node.js and Express.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Endpoints](#endpoints)
- [Contributing](#contributing)
- [License](#license)

## Installation

To set up the project locally, follow these steps:

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/user-registration-api.git
    cd user-registration-api
    ```

2. Install the dependencies:
    ```sh
    npm install
    ```

3. Create a `.env` file in the root of the project and add the necessary environment variables (e.g., database connection string).

4. Start the server:
    ```sh
    npm start
    ```

## Usage

After starting the server, the API will be available at `http://localhost:5000`.

### Example Request

You can use tools like Postman or curl to interact with the API. Here's an example using curl to register a new user:

```sh
curl -X POST http://localhost:5000/users -H "Content-Type: application/json" -d '{"firstName":"Jhonny","lastName":"Doe","age":10}'
```

## Endpoints

### POST /users

Registers a new user.

- **URL**: `/users`
- **Method**: `POST`
- **Headers**: `Content-Type: application/json`
- **Body**:
    ```json
    {
        "firstName": "Jhonny",
        "lastName": "Doe",
        "age": 10
    }
    ```

- **Success Response**:
    - **Code**: 200 OK
    - **Content**:
        ```json
        {
            "firstName": "Jhonny",
            "lastName": "Doe",
            "age": 10
        }
        ```

- **Error Response**:
    - **Code**: 400 Bad Request
    - **Content**: `{ error: "Invalid input" }`


