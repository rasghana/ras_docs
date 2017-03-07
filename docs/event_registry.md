### Register for one event
This enpoint allow users who have made payment to register for an event.

- Method: `POST`

- Endpoint: `https://api.example.org/api/v1/events/{eventid}/register-for-event/`

- User Authorization: ``Required`` 

          "Authorization": "Token xxxxxxxxxxxxxxxxxxxxx"

  - Request: ``[JSON Body]``

      - Note: Provide event id in the url ``{eventid}``,  user must be logged in with token and payment status must be provided in ``JSON Body``

            {
            "payment_status": "paid"
            }

 - Response: ``201 Created``

        {
          "status_code": 201,
          "message": "you have successfully registered for an event",
          "result": {
            "id": 13,
            "event": {
            "id": 2,
            "event_name": "Event 2",
            "venue": "Palace",
            "price": 500,
            "description": "second event",
            "created_date": "2017-02-14T14:47:12.191711Z",
            "modified_date": "2017-02-14T14:47:12.191734Z"
            },
            "user": 1,
            "unique_id": "278E1A5",
            "payment_status": "paid",
            "author": 1,
            "created_date": "2017-03-07",
            "modified_date": "2017-03-07"
          }
        }


- Error Response ``401 UNAUTHORIZED``

    - Already registered for that same event

              {
                "status_code": 401,
                "message": "You have already registered for this event"
               }

- Error Response ``400 BAD REQUEST``

    - User payment status is not paid

              {
                "status_code": 400,
                "message": "Unsuccessful event registration, check your payment status"
              }

### Get only events i have registered for
Allows a user to get access to all the events he has registered for.

- Method: `GET`

- Endpoint: `https://api.example.org/api/v1/events/my-events/`

- User Authorization: ``Required`` 

          "Authorization": "Token xxxxxxxxxxxxxxxxxxxx"

  - Response: ``200 ok``

        [
          {
            "id": 1,
            "event_name": "New Event",
            "venue": "Haatso",
            "price": 200,
            "description": "This is a brief description about the event",
            "created_date": "2017-02-14T12:39:58.407554Z",
            "modified_date": "2017-02-14T12:39:58.407577Z"
          },
          {
            "id": 2,
            "event_name": "Event 2",
            "venue": "Palace",
            "price": 500,
            "description": "second event",
            "created_date": "2017-02-14T14:47:12.191711Z",
            "modified_date": "2017-02-14T14:47:12.191734Z"
          }
        ]
