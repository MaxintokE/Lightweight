# User Management API

A RESTful API for managing users, allowing operations to create, retrieve, update, and delete user information.

## Table of Contents
- [Setup](#setup)
- [API Endpoints](#api-endpoints)
  - [Get User by ID](#get-user-by-id)
  - [Create User](#create-user)
  - [Update User](#update-user)
  - [Delete User](#delete-user)
- [Error Handling](#error-handling)
- [License](#license)
- [Contributing](#contributing)
- [Contact](#contact)

## Setup
1. Clone the repository:
   ```bash
   git clone <https://github.com/MaxintokE/Lightweight.git>
   ```
2. Navigate to the project directory:
   ```bash
   cd <https://github.com/MaxintokE/Lightweight>
   ```
3. Run the following command to install dependencies:
   ```bash
   npm install
   ```
4. Start the server:
   ```bash
   node index.js
   ```
5. The API will be available at `http://localhost:3000`.

## API Endpoints

### Get User by ID
- **URL**: `/api/users/:id`
- **Method**: `GET`
- **URL Params**: `id=[integer]`
- **Success Response**: 
  - **Code**: 200
  - **Content**: 
    ```json
    { 
      "id": 1, 
      "name": "John", 
      "email": "john@example.com" 
    }
    ```
- **Error Response**:
  - **Code**: 404
  - **Content**: 
    ```json
    { 
      "message": "User not found" 
    }
    ```

### Create User
- **URL**: `/api/users`
- **Method**: `POST`
- **Body Params**: 
  - `name=[string]`
  - `email=[string]`
- **Success Response**: 
  - **Code**: 201
  - **Content**: 
    ```json
    { 
      "id": 2, 
      "name": "Jane", 
      "email": "jane@example.com" 
    }
    ```
- **Error Response**:
  - **Code**: 400
  - **Content**: 
    ```json
    { 
      "message": "Invalid input" 
    }
    ```

### Update User
- **URL**: `/api/users/:id`
- **Method**: `PUT`
- **URL Params**: `id=[integer]`
- **Body Params**: 
  - `name=[string]` (optional)
  - `email=[string]` (optional)
- **Success Response**: 
  - **Code**: 200
  - **Content**: 
    ```json
    { 
      "id": 1, 
      "name": "John Updated", 
      "email": "john.updated@example.com" 
    }
    ```
- **Error Response**:
  - **Code**: 404
  - **Content**: 
    ```json
    { 
      "message": "User not found" 
    }
    ```

### Delete User
- **URL**: `/api/users/:id`
- **Method**: `DELETE`
- **URL Params**: `id=[integer]`
- **Success Response**: 
  - **Code**: 204
- **Error Response**:
  - **Code**: 404
  - **Content**: 
    ```json
    { 
      "message": "User not found" 
    }
    ```

## Error Handling
- The API uses standard HTTP status codes to indicate the success or failure of an API request.
- Common error responses include:
  - **400 Bad Request**: Returned when the request is invalid or missing parameters.
  - **404 Not Found**: Returned when the requested resource does not exist.
  - **500 Internal Server Error**: Returned when there is an unexpected error on the server side.

### Example Error Response
```json
{ 
  "message": "An error occurred" 
}
```

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a pull request.

## Contact
For questions or suggestions, please contact:
- **Name**: [himaxwell36@gmail.com]
- **GitHub**: [https://github.com/MaxintokE)
