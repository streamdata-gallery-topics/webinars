{
  "info": {
    "name": "GoToWebinar Get All Webinars",
    "_postman_id": "5791fff3-cf04-4021-9849-47f762c23b1a",
    "description": "Returns webinars scheduled for the future for a specified organizer.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Historical",
      "item": [
        {
          "id": "0261f7f4-71a5-4922-a2de-e4bc49e7c46f",
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
              "id": "4a5e91ca-1ea4-4a8c-be73-333746bf3834"
            }
          ]
        }
      ]
    },
    {
      "name": "Webinars",
      "item": [
        {
          "id": "587e3a4c-6fbc-4fbe-8cbd-eaaed3e59169",
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
              "id": "92ed97b1-52fc-4bfb-8060-60cd429bcbca"
            }
          ]
        }
      ]
    }
  ]
}