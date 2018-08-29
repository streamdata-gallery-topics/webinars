{
  "info": {
    "name": "Go To Webinar Get webinar meeting times",
    "_postman_id": "f0560164-f3bf-4af4-a6f0-dcec84837a02",
    "description": "Retrieves the meeting times for a webinar.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Organizers",
      "item": [
        {
          "id": "a5e4a57c-c6f7-4c3e-92b1-aa9595faca15",
          "name": "getWebinarMeetingTimes",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2W",
                "rest",
                "organizers/:organizerKey/webinars/:webinarKey/meetingtimes"
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
            "description": "Retrieves the meeting times for a webinar."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cb3913c8-7fe4-41fc-a3db-2a2af104bdcd"
            }
          ]
        }
      ]
    }
  ]
}