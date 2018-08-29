---
swagger: "2.0"
x-collection-name: LogMeIn
x-complete: 0
info:
  title: GoToWebinar Get webinar session
  description: Get webinar session.
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
  /{organizerKey}/upcomingWebinars:
    get:
      summary: Upcoming Webinars
      description: Returns webinars scheduled for the future for the specified organizer
        and webinars of other organizers where the specified organizer is a co-organizer.
      operationId: UpcomingWebinarsByOrganizerKeyGet
      x-api-path-slug: organizerkeyupcomingwebinars-get
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
      - Upcoming
      - Webinars
  /{organizerKey}/webinars/{webinarKey}/panelists:
    get:
      summary: Get webinar panelists
      description: Get webinar panelists.
      operationId: WebinarsPanelistsByOrganizerKeyAndWebinarKeyGet
      x-api-path-slug: organizerkeywebinarswebinarkeypanelists-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: path
        name: webinarKey
      responses:
        200:
          description: OK
      tags:
      - Webinar
      - Panelists
  /{organizerkey}/webinars:
    post:
      summary: Create Webinar
      description: Create webinar.
      operationId: WebinarsByOrganizerkeyPost
      x-api-path-slug: organizerkeywebinars-post
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: organizerkey
      responses:
        200:
          description: OK
      tags:
      - Webinar
  /{organizerKey}/webinars/{webinarKey}:
    get:
      summary: Get Webinar
      description: Get webinar.
      operationId: WebinarsByOrganizerKeyAndWebinarKeyGet
      x-api-path-slug: organizerkeywebinarswebinarkey-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: path
        name: webinarKey
      responses:
        200:
          description: OK
      tags:
      - Webinar
    put:
      summary: Update webinar
      description: Update webinar.
      operationId: WebinarsByOrganizerKeyAndWebinarKeyPut
      x-api-path-slug: organizerkeywebinarswebinarkey-put
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: path
        name: webinarKey
      responses:
        200:
          description: OK
      tags:
      - Webinar
    delete:
      summary: Cancel Webinar
      description: Cancel webinar.
      operationId: WebinarsByOrganizerKeyAndWebinarKeyDelete
      x-api-path-slug: organizerkeywebinarswebinarkey-delete
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: query
        name: sendCancellationEmails
      - in: path
        name: webinarKey
      responses:
        200:
          description: OK
      tags:
      - Cancel
      - Webinar
  /{organizerKey}/webinars/{webinarKey}/meetingtimes:
    get:
      summary: Get webinar meeting times
      description: Get webinar meeting times.
      operationId: WebinarsMeetingtimesByOrganizerKeyAndWebinarKeyGet
      x-api-path-slug: organizerkeywebinarswebinarkeymeetingtimes-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: path
        name: webinarKey
      responses:
        200:
          description: OK
      tags:
      - Webinar
      - Meeting
      - Times
  /{organizerKey}/webinars/{webinarKey}/performance:
    get:
      summary: Get performance for all webinar sessions
      description: Get performance for all webinar sessions.
      operationId: WebinarsPerformanceByOrganizerKeyAndWebinarKeyGet
      x-api-path-slug: organizerkeywebinarswebinarkeyperformance-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: path
        name: webinarKey
      responses:
        200:
          description: OK
      tags:
      - Performance
      - Webinar
      - Sessions
  /{organizerKey}/webinars/{webinarKey}/sessions:
    get:
      summary: Get webinar sessions
      description: Get webinar sessions.
      operationId: WebinarsSessionsByOrganizerKeyAndWebinarKeyGet
      x-api-path-slug: organizerkeywebinarswebinarkeysessions-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: path
        name: webinarKey
      responses:
        200:
          description: OK
      tags:
      - Webinar
      - Sessions
  /{organizerKey}/webinars/{webinarKey}/attendees:
    get:
      summary: Get attendees for all webinar sessions
      description: Get attendees for all webinar sessions.
      operationId: WebinarsAttendeesByOrganizerKeyAndWebinarKeyGet
      x-api-path-slug: organizerkeywebinarswebinarkeyattendees-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: path
        name: webinarKey
      responses:
        200:
          description: OK
      tags:
      - Attendees
      - Webinar
      - Sessions
  /{organizerKey}/webinars/{webinarKey}/panelists/{panelistKey}:
    delete:
      summary: Delete webinar panelist
      description: Delete webinar panelist.
      operationId: WebinarsPanelistsPanelistKeyByOrganizerKeyAndWebinarKeyDelete
      x-api-path-slug: organizerkeywebinarswebinarkeypanelistspanelistkey-delete
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: path
        name: panelistKey
      - in: path
        name: webinarKey
      responses:
        200:
          description: OK
      tags:
      - Webinar
      - Panelist
  /{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}:
    get:
      summary: Get webinar session
      description: Get webinar session.
      operationId: WebinarsSessionsSessionKeyByOrganizerKeyAndWebinarKeyGet
      x-api-path-slug: organizerkeywebinarswebinarkeysessionssessionkey-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: path
        name: sessionKey
      - in: path
        name: webinarKey
      responses:
        200:
          description: OK
      tags:
      - Webinar
      - Session
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