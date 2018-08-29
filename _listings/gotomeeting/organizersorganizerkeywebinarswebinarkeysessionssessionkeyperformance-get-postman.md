{
  "info": {
    "name": "Go To Webinar Get session performance",
    "_postman_id": "fdeb4747-33de-480d-88f1-93077d9ef0bc",
    "description": "Get performance details for a session. For technical reasons, this call cannot be executed from this documentation. Please use the curl command to execute it.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Organizers",
      "item": [
        {
          "id": "649d9fb3-b621-4caa-b96f-18b5785adcd5",
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
              "id": "1cb1ec76-15e4-41c0-a8ac-ee6a19cfadd3"
            }
          ]
        },
        {
          "id": "424b6bd3-1c40-4a2b-b6ce-cc6759bb89d6",
          "name": "getPerformance",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2W",
                "rest",
                "organizers/:organizerKey/webinars/:webinarKey/sessions/:sessionKey/performance"
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
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get performance details for a session. For technical reasons, this call cannot be executed from this documentation. Please use the curl command to execute it."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "aab63a8d-e3b7-4983-b539-8f51db4a0ea5"
            }
          ]
        }
      ]
    }
  ]
}