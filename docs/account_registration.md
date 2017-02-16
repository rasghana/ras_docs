### Account signup
`Endpoint: POST http://localhost:8000/api/v1/users/signup/`
  
  ``Request: [JSON Body]``

    {
    "email": "user@user.com",
    "password": "xxxxxxxx"
    }
  
  ``Response: 201 Created``

    {
    "email": "user@user.com",
    "token": "xxxxxxxxxxxxxxxxxx"
    }


### Account login
`Endpoint: POST http://localhost:8000/api/v1/users/login/`
  
  ``Request: [JSON Body]``

    {
    "email": "user@user.com",
    "password": "xxxxxxxx"
    }
  
  ``Response: 201 Created``

    {
    "email": "user@user.com",
    "token": "xxxxxxxxxxxxxxxxxx"
    }
