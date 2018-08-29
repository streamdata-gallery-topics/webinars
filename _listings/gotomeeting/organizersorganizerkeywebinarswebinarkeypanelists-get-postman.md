{
  "info": {
    "name": "Go To Webinar Get webinar panelists",
    "_postman_id": "34efba91-0335-4626-9285-edf7b3752856",
    "description": "Retrieves all the panelists for a specific webinar.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Organizers",
      "item": [
        {
          "id": "3543b131-5c01-4955-a591-429bcb88a772",
          "name": "getPanelists",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2W",
                "rest",
                "organizers/:organizerKey/webinars/:webinarKey/panelists"
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
            "description": "Retrieves all the panelists for a specific webinar."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "16c3d3e8-e45d-4444-a826-fcc3c953caaf"
            }
          ]
        }
      ]
    }
  ]
}