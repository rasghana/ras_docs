### Allows users to register

`Endpoint: POST http://localhost:8000/api/v1/registration/create-registration/`

  ``Request: [JSON Body]``

    {
      "first_name": "Kelvin",
      "middle_name": "Tetteh",
      "last_name": "Anyinatoe",
      "wassce_id_number": 1234568,
      "date_of_birth": "2017-02-10",
      "phone_number": 546424340,

    }

  `Response: 201`

     {
      "first_name": "Kelvin",
      "middle_name": "Tetteh",
      "last_name": "Anyinatoe",
      "wassce_id_number": 1234568,
      "date_of_birth": "2017-02-10",
      "phone_number": 546424340,
      "user": "token"
    }

### Get all registered users
`Endpoint: GET http://localhost:8000/api/v1/registration/`

  `Response: 200`

     [
      {
        "id": 3,
        "first_name": "Kennedy",
        "middle_name": "Martey",
        "last_name": "Anyinatoe",
        "wassce_id_number": 1233455,
        "date_of_birth": "2017-02-10",
        "phone_number": 246424340,
        "published_date": null,
        "created_date": "2017-02-10T22:07:12.709201Z",
        "modified": "2017-02-12T19:11:35.028970Z"
      },

      {
        "id": 4,
        "first_name": "Kelvin",
        "middle_name": "Tetteh",
        "last_name": "Anyinatoe",
        "wassce_id_number": 1234568,
        "date_of_birth": "2017-02-10",
        "phone_number": 546424340,
        "published_date": null,
        "created_date": "2017-02-12T22:37:50.108941Z",
        "modified": "2017-02-12T23:21:54.409830Z"
      }
    ]

### Edit registered user
`Endpoint: POST http://localhost:8000/api/v1/registration/{pk}/edit-registered-user/`
  
  ``Request: [JSON Body]``
  
      {
        "first_name": "Kelvin",
        "middle_name": "Tetteh",
        "last_name": "Anyinatoe",
        "wassce_id_number": 1234568,
        "date_of_birth": "2017-02-10",
        "phone_number": 546424340,
      }
      Response: 201
       {
        "first_name": "Kelvin",
        "middle_name": "Tetteh",
        "last_name": "Anyinatoe",
        "wassce_id_number": 1234568,
        "date_of_birth": "2017-02-10",
        "phone_number": 546424340,
      }
