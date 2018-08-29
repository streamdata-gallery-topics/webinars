{
  "info": {
    "name": "Go To Webinar Get performance for all webinar sessions",
    "_postman_id": "b66e5aaa-0047-45ad-8e1a-f646b396db28",
    "description": "Gets performance details for all sessions of a specific webinar.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Organizers",
      "item": [
        {
          "id": "a93ae7f6-e427-494b-b041-bde3a48f7e7b",
          "name": "getPerformanceForAllWebinarSessions",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2W",
                "rest",
                "organizers/:organizerKey/webinars/:webinarKey/performance"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "organizerKey",
                  "value": "organizerKey",
                  "type": "string"
                },
                {
                  "id": "webinarKey",
                  "value": "webinarKey",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets performance details for all sessions of a specific webinar."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f1d41552-a539-4491-9dcf-cdfed2e3f7fb"
            }
          ]
        }
      ]
    }
  ]
}