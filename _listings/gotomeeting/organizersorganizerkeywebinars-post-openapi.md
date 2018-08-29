---
swagger: "2.0"
x-collection-name: GoToMeeting
x-complete: 0
info:
  title: Go To Webinar Create webinar
  description: 'Creates a single session webinar, a sequence of webinars or a series
    of webinars depending on the type field in the body: "single_session" creates
    a single webinar session, "sequence" creates a webinar with multiple meeting times
    where attendees are expected to be the same for all sessions, and "series" creates
    a webinar with multiple meetings times where attendees choose only one to attend.
    The default, if no type is declared, is single_session. A sequence webinar requires
    a "recurrenceStart" object consisting of a "startTime" and "endTime" key for the
    first webinar of the sequence, a "recurrencePattern" of "daily", "weekly", "monthly",
    and a "recurrenceEnd" which is the last date of the sequence (for example, 2016-12-01).
    A series webinar requires a "times" array with a discrete "startTime" and "endTime"
    for each webinar in the series. The call requires a webinar subject and description.
    The "isPasswordProtected" sets whether the webinar requires a password for attendees
    to join. If set to True, the organizer must go to Registration Settings at My
    Webinars (https://global.gotowebinar.com/webinars.tmpl) and add the password to
    the webinar, and send the password to the registrants. The response provides a
    numeric webinarKey in string format for the new webinar. Once a webinar has been
    created with this method, you can accept registrations.'
  termsOfService: https://developer.citrixonline.com/terms-use
  contact:
    name: Developer Support
    url: https://developer.citrixonline.com
    email: developer-support@citrixonline.com
  version: 1.0.0
host: api.citrixonline.com
basePath: /G2W/rest
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /accounts/{accountKey}/webinars:
    get:
      summary: Get all webinars for an account
      description: Retrieves the list of webinars for an account within a given date
        range. __*Page*__ and __*size*__ parameters are optional. Default __*page*__
        is 0 and default __*size*__ is 20. For technical reasons, this call cannot
        be executed from this documentation. Please use the curl command to execute
        it.
      operationId: getAllAccountWebinars
      x-api-path-slug: accountsaccountkeywebinars-get
      parameters:
      - in: query
        name: fromTime
        description: A required start of datetime range in ISO8601 UTC format, e
      - in: query
        name: No Name
      - in: query
        name: page
        description: The page number to be displayed
      - in: query
        name: size
        description: The size of the page
      - in: query
        name: toTime
        description: A required end of datetime range in ISO8601 UTC format, e
      responses:
        200:
          description: OK
      tags:
      - Accounts
      - AccountKey
      - Webinars
  /organizers/{organizerKey}/webinars:
    get:
      summary: Get all webinars
      description: Returns webinars scheduled for the future for a specified organizer.
      operationId: getAllWebinars
      x-api-path-slug: organizersorganizerkeywebinars-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
    post:
      summary: Create webinar
      description: 'Creates a single session webinar, a sequence of webinars or a
        series of webinars depending on the type field in the body: "single_session"
        creates a single webinar session, "sequence" creates a webinar with multiple
        meeting times where attendees are expected to be the same for all sessions,
        and "series" creates a webinar with multiple meetings times where attendees
        choose only one to attend. The default, if no type is declared, is single_session.
        A sequence webinar requires a "recurrenceStart" object consisting of a "startTime"
        and "endTime" key for the first webinar of the sequence, a "recurrencePattern"
        of "daily", "weekly", "monthly", and a "recurrenceEnd" which is the last date
        of the sequence (for example, 2016-12-01). A series webinar requires a "times"
        array with a discrete "startTime" and "endTime" for each webinar in the series.
        The call requires a webinar subject and description. The "isPasswordProtected"
        sets whether the webinar requires a password for attendees to join. If set
        to True, the organizer must go to Registration Settings at My Webinars (https://global.gotowebinar.com/webinars.tmpl)
        and add the password to the webinar, and send the password to the registrants.
        The response provides a numeric webinarKey in string format for the new webinar.
        Once a webinar has been created with this method, you can accept registrations.'
      operationId: createWebinar
      x-api-path-slug: organizersorganizerkeywebinars-post
      parameters:
      - in: body
        name: body
        description: The webinar details
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
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