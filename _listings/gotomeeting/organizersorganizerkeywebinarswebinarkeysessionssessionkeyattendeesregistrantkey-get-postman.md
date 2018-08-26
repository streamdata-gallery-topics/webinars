{
  "info": {
    "name": "Go To Webinar Get attendee",
    "_postman_id": "e63c05d6-668d-45bb-a054-6bc84ef92ed6",
    "description": "Retrieve registration details for a particular attendee of a specific webinar session. For technical reasons, this call cannot be executed from this documentation. Please use the curl command to execute it.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Organizers",
      "item": [
        {
          "id": "273d88fd-9f99-45c6-9a27-565e6d06311c",
          "name": "getOrganizerSessions",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2W",
                "rest",
                "organizers/:organizerKey/sessions"
              ],
              "query": [
                {
                  "key": "fromTime",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "No Name",
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
                  "value": "organizerKey",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve all completed sessions of all the webinars of a given organizer."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d13746d9-dd0d-4add-8ae5-4498d26ba165"
            }
          ]
        },
        {
          "id": "86533727-0e6f-475a-8999-eb1f2b6aacab",
          "name": "getAllSessions",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2W",
                "rest",
                "organizers/:organizerKey/webinars/:webinarKey/sessions"
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
            "description": "Retrieves details for all past sessions of a specific webinar."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e6ebc734-cad8-417e-91ab-346da742eaa6"
            }
          ]
        },
        {
          "id": "d06ee3d6-7dd7-4bd5-a446-07410a2740df",
          "name": "getWebinarSession",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2W",
                "rest",
                "organizers/:organizerKey/webinars/:webinarKey/sessions/:sessionKey"
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
            "description": "Retrieves attendance details for a specific webinar session that has ended. If attendees attended the session ('registrantsAttended'), specific attendance details, such as attendenceTime for a registrant, will also be retrieved. For technical reasons, this call cannot be executed from this documentation. Please use the curl command to execute it."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "db309213-ef30-4e2f-b147-f584c2733f82"
            }
          ]
        },
        {
          "id": "d2377754-70d1-47b8-8637-9da3623b24d6",
          "name": "getAttendees",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2W",
                "rest",
                "organizers/:organizerKey/webinars/:webinarKey/sessions/:sessionKey/attendees"
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
            "description": "Retrieve details for all attendees of a specific webinar session. For technical reasons, this call cannot be executed from this documentation. Please use the curl command to execute it."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2f5eb413-149d-402e-bd0f-9968934d1365"
            }
          ]
        },
        {
          "id": "d9675227-41aa-4d4e-b7be-e986899450b9",
          "name": "getAttendee",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2W",
                "rest",
                "organizers/:organizerKey/webinars/:webinarKey/sessions/:sessionKey/attendees/:registrantKey"
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
            "description": "Retrieve registration details for a particular attendee of a specific webinar session. For technical reasons, this call cannot be executed from this documentation. Please use the curl command to execute it."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a64a5e0d-ae11-4e2c-b795-24955bbc7304"
            }
          ]
        }
      ]
    }
  ]
}