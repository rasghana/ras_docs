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
