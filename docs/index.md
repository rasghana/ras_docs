# Welcome to Ras api documentation

Welcome to Ras Event app. visit [rasghana.com](http://www.rasghana.com) for more information on the app

Quick notes

This section describes the usage of the RAS Ghana Mobile API. To get started. To fully implement the mobile API, you must understand following standards.

Official API for the RAS Ghana Mobile Applications

### Base URLs

 - To test the api on stage or development server, use: ``http://stage.rasghana.org/api/v1/``
 - To use the live or production api, use: ``http://rasghana.org/api/v1/`` as your base URL. The base url must preceed all endpoints used to interact with the API server.


### API Responses

Generally, all API responses are returned in the standard `JSON` format.

### Good Response

The standard HTTP response code which occures when data is submitted or data is fetched begins with `2` e.g. , `200 Ok`, `201 Created`, You will have a standard json response with a format:

    {
         "status_code": 200,
         "message": "You have fetched all the data",
         "results": [
         ....................
         ]
    }

The ``status_code`` in the response body describes the internal status code which describes the `message` of the error. The details describe the exact error that occurred and the results brings out the response of the request,


### Error Codes

Apart from the standard HTTP errors, there are errors codes which can be returned when something goes wrong. When an error with HTTP error code begins with `4` e.g. `400 (Bad Request)`, `401 (UnAuthorized)` You will have a standard json response with a format:

    {
         "status_code": 400,
         "message": "Bad request. Data was not saved. Please check the fields and data you are submitting"
    }

The ``status_code`` in the response body describes the internal status code which describes the `message` of the error. The details describe the exact error that occurred.

### Owner

RAS Ghana.

### Developer

Kennedy Anyinatoe.
