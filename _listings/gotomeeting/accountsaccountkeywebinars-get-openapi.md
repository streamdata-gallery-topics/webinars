---
swagger: "2.0"
x-collection-name: GoToMeeting
x-complete: 0
info:
  title: Go To Webinar Get all webinars for an account
  description: Retrieves the list of webinars for an account within a given date range.
    __*Page*__ and __*size*__ parameters are optional. Default __*page*__ is 0 and
    default __*size*__ is 20. For technical reasons, this call cannot be executed
    from this documentation. Please use the curl command to execute it.
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