{
  "info": {
    "name": "Go To Webinar Get audio information",
    "_postman_id": "1f2bf65e-95c7-4d48-9ffe-593341226940",
    "description": "Retrieves the audio/conferencing information for a specific webinar.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Organizers",
      "item": [
        {
          "id": "f1847e18-5471-4e86-915e-a26406b9d45e",
          "name": "getAudioInformation",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2W",
                "rest",
                "organizers/:organizerKey/webinars/:webinarKey/audio"
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
            "description": "Retrieves the audio/conferencing information for a specific webinar."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "98a4b176-9646-41b9-96f2-4ceb3446d939"
            }
          ]
        }
      ]
    }
  ]
}