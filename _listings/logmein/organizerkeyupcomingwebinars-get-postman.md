{
  "info": {
    "name": "GoToWebinar Upcoming Webinars",
    "_postman_id": "ea046c94-3a08-4ad1-a880-8bd12d3fcf13",
    "description": "Returns webinars scheduled for the future for the specified organizer and webinars of other organizers where the specified organizer is a co-organizer.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Historical",
      "item": [
        {
          "id": "6010155e-7c9e-4c76-906e-fcfa43b44259",
          "name": "HistoricalWebinarsByOrganizerKeyGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.getgo.com",
              "path": [
                "G2W",
                "rest",
                "organizers",
                ":organizerKey/historicalWebinars"
              ],
              "query": [
                {
                  "key": "fromTime",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "toTime",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "organizerKey",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Content-Type",
                "value": "{}",
                "description": "",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns details for completed webinars for the specified organizer and completed webinars of other organizers where the specified organizer is a co-organizer.\n\nParameters:\n- organizerkey \n- fromTime\n- toTime"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3dfbe29d-9400-4d5c-af7a-db528b5cbba4"
            }
          ]
        }
      ]
    },
    {
      "name": "Webinars",
      "item": [
        {
          "id": "152341d7-1e08-4a07-9ca0-15f02ab0ba8f",
          "name": "WebinarsByOrganizerKeyGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.getgo.com",
              "path": [
                "G2W",
                "rest",
                "organizers",
                ":organizerKey/webinars"
              ],
              "variable": [
                {
                  "id": "organizerKey",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Content-Type",
                "value": "{}",
                "description": "",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns webinars scheduled for the future for a specified organizer."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bdac9f04-2fe3-4084-ac02-691d099f9cea"
            }
          ]
        }
      ]
    },
    {
      "name": "Upcoming",
      "item": [
        {
          "id": "2212d53a-6022-4c37-b80c-9597bbb3afe9",
          "name": "UpcomingWebinarsByOrganizerKeyGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.getgo.com",
              "path": [
                "G2W",
                "rest",
                "organizers",
                ":organizerKey/upcomingWebinars"
              ],
              "variable": [
                {
                  "id": "organizerKey",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Content-Type",
                "value": "{}",
                "description": "",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns webinars scheduled for the future for the specified organizer and webinars of other organizers where the specified organizer is a co-organizer."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "82985b91-9a72-4e00-9f1f-a1c746b9cd3f"
            }
          ]
        }
      ]
    }
  ]
}