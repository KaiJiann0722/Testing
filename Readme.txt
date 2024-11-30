# API Paths for Testing

Below are the API paths that you can test. Please ensure the server is running before sending requests.

## 1. User Authentication

- **POST** `/token/login/`
  - Description: Logs in a user and returns a token for authentication.
  - Example:
    ```
    {
      "username": "testuser",
      "password": "password123"
    }
    ```

- **POST** `/token/logout/`
  - Description: Logs out the user by invalidating the token.

## 2. User Information

- **GET** `/users/me/`
  - Description: Retrieves the current logged-in user's details.
  - Headers:
    - Authorization: Bearer {your_token}

## 3. Cars API

- **GET** `/cars/`
  - Description: Retrieves a list of cars available.
  
- **POST** `/cars/`
  - Description: Adds a new car to the inventory.
  - Example:
    ```
    {
      "make": "Toyota",
      "model": "Corolla",
      "year": 2020,
      "price": 20000
    }
    ```

- **PUT** `/cars/{id}/`
  - Description: Updates a specific car by its ID.
  - Example:
    ```
    {
      "make": "Honda",
      "model": "Civic",
      "year": 2021,
      "price": 22000
    }
    ```

- **DELETE** `/cars/{id}/`
  - Description: Deletes a car by its ID.
  
## 4. Orders API

- **GET** `/orders/`
  - Description: Retrieves all orders made by the user.

- **POST** `/orders/`
  - Description: Places a new order.
  - Example:
    ```
    {
      "car_id": 1,
      "quantity": 2,
      "delivery_address": "123 Main St, Kuala Lumpur"
    }
    ```

---

   
