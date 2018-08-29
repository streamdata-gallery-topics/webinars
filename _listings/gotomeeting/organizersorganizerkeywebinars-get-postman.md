{
  "info": {
    "name": "Go To Webinar Get all webinars",
    "_postman_id": "a6f50691-1811-403a-b366-88e883548159",
    "description": "Returns webinars scheduled for the future for a specified organizer.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Accounts",
      "item": [
        {
          "id": "b557531a-0239-4655-9c60-aab0468c35cd",
          "name": "getAllAccountWebinars",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2W",
                "rest",
                "accounts/:accountKey/webinars"
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
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "size",
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
                  "id": "accountKey",
                  "value": "accountKey",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the list of webinars for an account within a given date range. __*Page*__ and __*size*__ parameters are optional. Default __*page*__ is 0 and default __*size*__ is 20. For technical reasons, this call cannot be executed from this documentation. Please use the curl command to execute it."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5498f1b1-f241-4784-a8b7-e971be3a6819"
            }
          ]
        }
      ]
    },
    {
      "name": "Organizers",
      "item": [
        {
          "id": "50cce3a3-4c6b-4729-9795-542413324c9b",
          "name": "getHistoricalWebinars",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2W",
                "rest",
                "organizers/:organizerKey/historicalWebinars"
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
            "description": "Returns details for completed webinars for the specified organizer and completed webinars of other organizers where the specified organizer is a co-organizer."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "71166f0b-da95-4d45-81f5-5e9caa45194a"
            }
          ]
        },
        {
          "id": "53b0ed58-4e11-4438-a08c-8e8db0c41b31",
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
              "id": "ceb296b0-593a-43ee-a513-f5f1c931f27f"
            }
          ]
        },
        {
          "id": "9e7c9491-919e-4a38-8264-dad9dbd157d6",
          "name": "getUpcomingWebinars",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2W",
                "rest",
                "organizers/:organizerKey/upcomingWebinars"
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
                }
              ]
            },
            "method": "GET",
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
              "id": "66343a2a-5b0d-4218-9d25-f5c0380c0696"
            }
          ]
        },
        {
          "id": "5a76ce20-2c1a-43cd-9223-eeec69abc9b7",
          "name": "getAllWebinars",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2W",
                "rest",
                "organizers/:organizerKey/webinars"
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
                }
              ]
            },
            "method": "GET",
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
              "id": "f2c053a7-587d-4e36-b991-661fd77682c2"
            }
          ]
        }
      ]
    }
  ]
}