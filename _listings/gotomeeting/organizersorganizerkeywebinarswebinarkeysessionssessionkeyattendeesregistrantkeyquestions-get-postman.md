{
  "info": {
    "name": "Go To Webinar Get attendee questions",
    "_postman_id": "637d8004-3961-4c03-b460-36db2a398e25",
    "description": "Get questions asked by an attendee during a webinar session. For technical reasons, this call cannot be executed from this documentation. Please use the curl command to execute it.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Organizers",
      "item": [
        {
          "id": "ea917862-d790-4615-8c10-a881c1568b9a",
          "name": "getAttendeeQuestions",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2W",
                "rest",
                "organizers/:organizerKey/webinars/:webinarKey/sessions/:sessionKey/attendees/:registrantKey/questions"
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
                },
                {
                  "id": "sessionKey",
                  "value": "sessionKey",
                  "type": "string"
                },
                {
                  "id": "registrantKey",
                  "value": "registrantKey",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get questions asked by an attendee during a webinar session. For technical reasons, this call cannot be executed from this documentation. Please use the curl command to execute it."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "45324a00-1aa8-4c22-9805-804bcb8874ef"
            }
          ]
        }
      ]
    }
  ]
}