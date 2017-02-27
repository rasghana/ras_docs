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
        "email": "user@user.com",
        "auth_token": "xxxxxxxxxxxxxxxxxxxxxx"
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
        "email": "user@user.com",
        "auth_token": "xxxxxxxxxxxxxxxxxxxxx"
        }
