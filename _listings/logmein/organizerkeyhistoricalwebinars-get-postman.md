{
  "info": {
    "name": "GoToWebinar Historical Webinars",
    "_postman_id": "13c82895-2207-4167-8104-0482cb66a70f",
    "description": "Returns details for completed webinars for the specified organizer and completed webinars of other organizers where the specified organizer is a co-organizer.\n\nParameters:\n- organizerkey \n- fromTime\n- toTime",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Historical",
      "item": [
        {
          "id": "ad53f03a-0f69-4770-82d7-b37d996755bb",
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
              "id": "d3abb816-c4d1-4659-b536-9e4c468c7355"
            }
          ]
        }
      ]
    }
  ]
}