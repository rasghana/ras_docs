### Account signup
`Endpoint: POST https://api.example.org/api/v1/users/signup/`
  
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
`Endpoint: POST https://api.example.org/api/v1/users/login/`
  
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
