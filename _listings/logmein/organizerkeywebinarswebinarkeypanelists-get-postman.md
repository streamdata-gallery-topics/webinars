{
  "info": {
    "name": "GoToWebinar Get webinar panelists",
    "_postman_id": "6db01158-2d7c-48c9-a018-b6650fcedd16",
    "description": "Get webinar panelists.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Webinar",
      "item": [
        {
          "id": "5082c715-b53f-4444-b371-a364e0d1c91a",
          "name": "WebinarsPanelistsByOrganizerKeyAndWebinarKeyGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.getgo.com",
              "path": [
                "G2W",
                "rest",
                "organizers",
                ":organizerKey/webinars/:webinarKey/panelists"
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
            "description": "Get webinar panelists."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dba63941-9f4b-4000-b75e-c284411cd1a3"
            }
          ]
        }
      ]
    }
  ]
}