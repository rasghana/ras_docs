### Allows users to register

- Method: `POST`

- Endpoint: `https://api.example.org/api/v1/registration/create-registration/`

- User Authorization: ``Required`` 

          "Authorization": "Token xxxxxxxxxxxxxxxxxx"

  - Request: ``[JSON Body]``

        {
          "first_name": "Kelvin",
          "middle_name": "Tetteh",
          "last_name": "Anyinatoe",
          "wassce_id_number": 1234568,
          "date_of_birth": "2017-02-10",
          "phone_number": 546424340,
        }

  - Response: `201 Created`

         {
          "first_name": "Kelvin",
          "middle_name": "Tetteh",
          "last_name": "Anyinatoe",
          "wassce_id_number": 1234568,
          "date_of_birth": "2017-02-10",
          "phone_number": 546424340,
          "published_date": null,
          "created_date": "2017-02-27T19:49:14.212813Z",
          "modified": "2017-02-27T19:49:14.212846Z"
        }

### Get all registered users

- Method: `GET`

- Endpoint: `https://api.example.org/api/v1/registration/`

- User Authorization: ``Required`` 

          "Authorization": "Token xxxxxxxxxxxxxxxxxx"

  - Response: `200 Ok`

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

- Method: `POST`

- Endpoint: `https://api.example.org/api/v1/registration/{pk}/edit-registered-user/`

  - User Authorization: ``Required`` 

          "Authorization": "Token xxxxxxxxxxxxxxxxxx"

  - Request: ``[JSON Body]``
  
          {
            "first_name": "Kelvin",
            "middle_name": "Tetteh",
            "last_name": "Anyinatoe",
            "wassce_id_number": 1234568,
            "date_of_birth": "2017-02-10",
            "phone_number": 546424340,
          }

  - Response: `201 Created`

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
