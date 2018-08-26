---
swagger: "2.0"
x-collection-name: LogMeIn
x-complete: 0
info:
  title: GoToWebinar Get All Webinars
  description: Returns webinars scheduled for the future for a specified organizer.
  version: 1.0.0
host: api.getgo.com
basePath: /G2W/rest/organizers
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{organizerKey}/historicalWebinars:
    get:
      summary: Historical Webinars
      description: "Returns details for completed webinars for the specified organizer
        and completed webinars of other organizers where the specified organizer is
        a co-organizer.\n\nParameters:\n- organizerkey \n- fromTime\n- toTime"
      operationId: HistoricalWebinarsByOrganizerKeyGet
      x-api-path-slug: organizerkeyhistoricalwebinars-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: query
        name: fromTime
      - in: path
        name: organizerKey
      - in: query
        name: toTime
      responses:
        200:
          description: OK
      tags:
      - Historical
      - Webinars
  /{organizerKey}/webinars:
    get:
      summary: Get All Webinars
      description: Returns webinars scheduled for the future for a specified organizer.
      operationId: WebinarsByOrganizerKeyGet
      x-api-path-slug: organizerkeywebinars-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      responses:
        200:
          description: OK
      tags:
      - Webinars
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---