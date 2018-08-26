{
  "info": {
    "name": "GoToWebinar Get webinar meeting times",
    "_postman_id": "e515c8c7-9c35-4044-b321-ff47e0098383",
    "description": "Get webinar meeting times.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Webinar",
      "item": [
        {
          "id": "c13fd616-a723-4be4-bf37-47d5a5e9ede7",
          "name": "WebinarsMeetingtimesByOrganizerKeyAndWebinarKeyGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.getgo.com",
              "path": [
                "G2W",
                "rest",
                "organizers",
                ":organizerKey/webinars/:webinarKey/meetingtimes"
              ],
              "variable": [
                {
                  "id": "organizerKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "webinarKey",
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
            "description": "Get webinar meeting times."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "381133a9-d50d-46db-9264-ace30829331b"
            }
          ]
        }
      ]
    }
  ]
}