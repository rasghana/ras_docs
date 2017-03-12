### Account signup

- Method: `POST`

- Endpoint: `https://api.example.org/api/v1/users/signup/`
  
  - Request: ``[JSON Body]``

        {
        "email": "user@user.com",
        "password": "xxxxxxxx"
        }
      
  - Response: ``201 Created``

        {
          "status_code": 201,
          "message": "you have successfully signed up on Ras",
          "result": {
            "email": "user@user.com",
            "auth_token": "xxxxxxxxxxxxxxxxxxxxxx"
          }
        }

  - Error Response ``401 UNAUTHORIZED``

    - Invalid email error

            {
            "status_code": 401,
            "message": "please enter a valid email address",
            }

   - Error Response ``401 UNAUTHORIZED``

    - Email already exist

            {
            "status_code": 401,
            "message": "email already exist, please use different email"
            }

### Account login

- Method: `POST`

- Endpoint: `https://api.example.org/api/v1/users/login/`
  
  - Request: ``[JSON Body]``

        {
        "email": "user@user.com",
        "password": "xxxxxxxx"
        }
  
  - Response: ``201 Created``

        {
        "status_code": 200,
        "message": "you have successfully logged in",
        "result": {
          "email": "kk@kk.com",
          "auth_token": "xxxxxxxxxxxxxxxxxxxxxxxxxxx"
          }
        }

- Error Response ``404 NOT FOUND``

    - Account deactivated

            {
            "status_code": 404,
             "message": "This account has been deactivated"
            }

- Error Response ``400 BAD REQUEST``

    - Invalid username or password

            {
            "status_code": 400,
             "message": "Invalid username or password"
            }


### Retrieve a logged in user

- Method: ``GET``

- Endpoint: `https://api.example.org/api/v1/users/{userid}/`

    - Authorization: ``Token xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx``

            {
            "id": 1,
            "email": "xxxxxx@xxxxxxx.com",
            "auth_token": "xxxxxxxxxxxxxxxxxxxxxxxxxx"
            }

- Error Response ``401 UNAUTHORIZED``

    - Please provide Token

            {
            "detail": "Authentication credentials were not provided."
            }


### Logout a user

- Method: ``POST``

- Endpoint: `https://api.example.org/api/v1/users/{userid}/logout/`

    - Authorization: ``Token xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx``

        - Response: ``200 OK``

                {
                "status_code": 200,
                "message": "You have been successfully logged out"
                }

       - Note: The token expires and and new one is genenrated for new login session.


- Error Response ``401 UNAUTHORIZED``

When a user is logged out for the first time, the token expires and a new one is generated. When you hit the endpoint agian with the previous token, You get Invalide token error

  - Invalid Token

        {
        "message": "Invalid Token"
        }

