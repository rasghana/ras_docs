## Get all events

All events are entered from the dashboard. This endpoint shows all list of events from in the system

- Method: `GET`

- Endpoint: `https://api.example.org/api/v1/events/`

  - Response: ``200 ok``

        {
          "count": 2,
          "next": null,
          "previous": null,
          "results": [
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
        }

