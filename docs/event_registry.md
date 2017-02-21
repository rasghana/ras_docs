### Register for one event
`Endpoint: GET https://api.example.org/api/v1/events/{pk}/register-for-event/`

  ``Response: 201 Created``

    {
      "id": 11,
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
      "unique_id": "BDD1535",
      "payment_status": "paid",
      "author": 1,
      "created_date": "2017-02-16",
      "modified_date": "2017-02-16"
    }


### Get only events i have registered for
`Endpoint: GET https://api.example.org/api/v1/events/my-events/`

  ``Response: 200 ok``

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
