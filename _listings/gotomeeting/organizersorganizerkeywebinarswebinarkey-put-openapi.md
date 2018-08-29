---
swagger: "2.0"
x-collection-name: GoToMeeting
x-complete: 0
info:
  title: Go To Webinar Update webinar
  description: Updates a webinar. The call requires at least one of the parameters
    in the request body. The request completely replaces the existing session, series,
    or sequence and so must include the full definition of each as for the Create
    call. Set notifyParticipants=true to send update emails to registrants.
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
  /organizers/{organizerKey}/webinars/{webinarKey}:
    delete:
      summary: Cancel webinar
      description: Cancels a specific webinar. If the webinar is a series or sequence,
        this call deletes all scheduled sessions. To send cancellation emails to registrants
        set sendCancellationEmails=true in the request. When the cancellation emails
        are sent, the default generated message is used in the cancellation email
        body.
      operationId: cancelWebinar
      x-api-path-slug: organizersorganizerkeywebinarswebinarkey-delete
      parameters:
      - in: query
        name: No Name
      - in: query
        name: sendCancellationEmails
        description: Indicates whether cancellation notice emails should be sent
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
    get:
      summary: Get webinar
      description: Retrieve information on a specific webinar. If the type of the
        webinar is 'sequence', a sequence of future times will be provided. Webinars
        of type 'series' are treated the same as normal webinars - each session in
        the webinar series has a different webinarKey. If an organizer cancels a webinar,
        then a request to get that webinar would return a '404 Not Found' error.
      operationId: getWebinar
      x-api-path-slug: organizersorganizerkeywebinarswebinarkey-get
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
      - WebinarKey
    put:
      summary: Update webinar
      description: Updates a webinar. The call requires at least one of the parameters
        in the request body. The request completely replaces the existing session,
        series, or sequence and so must include the full definition of each as for
        the Create call. Set notifyParticipants=true to send update emails to registrants.
      operationId: updateWebinar
      x-api-path-slug: organizersorganizerkeywebinarswebinarkey-put
      parameters:
      - in: body
        name: body
        description: The webinar details
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      - in: query
        name: notifyParticipants
        description: Defines whether to send notifications to participants
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
  /organizers/{organizerKey}/webinars/{webinarKey}/attendees:
    get:
      summary: Get attendees for all webinar sessions
      description: Returns all attendees for all sessions of the specified webinar.
      operationId: getAttendeesForAllWebinarSessions
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeyattendees-get
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
      - WebinarKey
      - Attendees
  /organizers/{organizerKey}/webinars/{webinarKey}/audio:
    get:
      summary: Get audio information
      description: Retrieves the audio/conferencing information for a specific webinar.
      operationId: getAudioInformation
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeyaudio-get
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
      - WebinarKey
      - Audio
    post:
      summary: Update audio information
      description: Updates the audio/conferencing settings for a specific webinar
      operationId: updateAudioInformation
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeyaudio-post
      parameters:
      - in: body
        name: body
        description: The audio/conferencing settings
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      - in: query
        name: notifyParticipants
        description: Defines whether to send notifications to participants
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
      - Audio
  /organizers/{organizerKey}/webinars/{webinarKey}/coorganizers:
    get:
      summary: Get co-organizers
      description: Returns the co-organizers for the specified webinar. The original
        organizer who created the webinar is filtered out of the list. If the webinar
        has no co-organizers, an empty array is returned. Co-organizers that do not
        have a GoToWebinar account are returned as external co-organizers. For those
        organizers no surname is returned.
      operationId: getCoorganizers
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeycoorganizers-get
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
      - WebinarKey
      - Coorganizers
    post:
      summary: Create co-organizers
      description: Creates co-organizers for the specified webinar. For co-organizers
        that have a GoToWebinar account you have to set the parameter 'external' to
        'false'. In this case you have to pass the parameter 'organizerKey' only.
        For co-organizers that have no GoToWebinar account you have to set the parameter
        'external' to 'true'. In this case you have to pass the parameters 'givenName'
        and 'email'. Since there is no parameter for 'surname' you should pass first
        and last name to the parameter 'givenName'.
      operationId: createCoorganizers
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeycoorganizers-post
      parameters:
      - in: body
        name: body
        description: The co-organizer details
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
      - WebinarKey
      - Coorganizers
  /organizers/{organizerKey}/webinars/{webinarKey}/coorganizers/{coorganizerKey}:
    delete:
      summary: Delete co-organizer
      description: Deletes an internal co-organizer specified by the coorganizerKey
        (memberKey).
      operationId: deleteCoorganizer
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkey-delete
      parameters:
      - in: query
        name: external
        description: By default only internal co-organizers (with a GoToWebinar account)
          can be deleted
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
      - Coorganizers
      - CoorganizerKey
  /organizers/{organizerKey}/webinars/{webinarKey}/coorganizers/{coorganizerKey}/resendInvitation:
    post:
      summary: Resend invitation
      description: Resends an invitation email to the specified co-organizer
      operationId: resendCoorganizerInvitation
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkeyresendinvitation-post
      parameters:
      - in: query
        name: external
        description: By default only internal co-organizers (with a GoToWebinar account)
          will retrieve the resent invitation email
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
      - Coorganizers
      - CoorganizerKey
      - ResendInvitation
  /organizers/{organizerKey}/webinars/{webinarKey}/meetingtimes:
    get:
      summary: Get webinar meeting times
      description: Retrieves the meeting times for a webinar.
      operationId: getWebinarMeetingTimes
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeymeetingtimes-get
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
      - WebinarKey
      - Meetingtimes
  /organizers/{organizerKey}/webinars/{webinarKey}/panelists:
    get:
      summary: Get webinar panelists
      description: Retrieves all the panelists for a specific webinar.
      operationId: getPanelists
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeypanelists-get
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
      - WebinarKey
      - Panelists
    post:
      summary: Create Panelists
      description: Create panelists for a specified webinar
      operationId: createPanelists
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeypanelists-post
      parameters:
      - in: body
        name: body
        description: Array of panelists
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
      - WebinarKey
      - Panelists
  /organizers/{organizerKey}/webinars/{webinarKey}/panelists/{panelistKey}:
    delete:
      summary: Delete webinar panelist
      description: Removes a webinar panelist.
      operationId: deleteWebinarPanelist
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeypanelistspanelistkey-delete
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
      - WebinarKey
      - Panelists
      - PanelistKey
  /organizers/{organizerKey}/webinars/{webinarKey}/panelists/{panelistKey}/resendInvitation:
    post:
      summary: Resend panelist invitation
      description: Resend the panelist invitation email.
      operationId: resendPanelistInvitation
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeypanelistspanelistkeyresendinvitation-post
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
      - WebinarKey
      - Panelists
      - PanelistKey
      - ResendInvitation
  /organizers/{organizerKey}/webinars/{webinarKey}/performance:
    get:
      summary: Get performance for all webinar sessions
      description: Gets performance details for all sessions of a specific webinar.
      operationId: getPerformanceForAllWebinarSessions
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeyperformance-get
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
      - WebinarKey
      - Performance
  /organizers/{organizerKey}/webinars/{webinarKey}/registrants:
    get:
      summary: Get registrants
      description: Retrieve registration details for all registrants of a specific
        webinar. Registrant details will not include all fields captured when creating
        the registrant. To see all data, use the API call 'Get Registrant'. Registrants
        can have one of the following states; <br>WAITING - registrant registered
        and is awaiting approval (where organizer has required approval), <br>APPROVED
        - registrant registered and is approved, and <br>DENIED - registrant registered
        and was denied.
      operationId: getAllRegistrantsForWebinar
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeyregistrants-get
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
      - WebinarKey
      - Registrants
    post:
      summary: Create registrant
      description: 'Register an attendee for a scheduled webinar. The response contains
        the registrantKey and join URL for the registrant. An email will be sent to
        the registrant unless the organizer turns off the confirmation email setting
        from the GoToWebinar website. Please note that you must provide all required
        fields including custom fields defined during the webinar creation. Use the
        API call ''Get registration fields'' to get a list of all fields, if they
        are required, and their possible values. At this time there are two versions
        of the ''Create Registrant'' call. The first version only accepts firstName,
        lastName, and email and ignores all other fields. If you have custom fields
        or want to capture additional information this version won''t work for you.
        The second version allows you to pass all required and optional fields, including
        custom fields defined when creating the webinar. To use the second version
        you must pass the header value ''Accept: application/vnd.citrix.g2wapi-v1.1+json''
        instead of ''Accept: application/json''. Leaving this header out results in
        the first version of the API call.'
      operationId: createRegistrant
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeyregistrants-post
      parameters:
      - in: header
        name: Accept
        description: Set to application/vnd
      - in: body
        name: body
        description: The registrant details
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      - in: query
        name: resendConfirmation
        description: Indicates whether the confirmation email should be resent when
          a registrant is re-registered
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
      - Registrants
  /organizers/{organizerKey}/webinars/{webinarKey}/registrants/fields:
    get:
      summary: Get registration fields
      description: Retrieve required, optional registration, and custom questions
        for a specified webinar.
      operationId: getRegistrationFields
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeyregistrantsfields-get
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
      - WebinarKey
      - Registrants
      - Fields
  /organizers/{organizerKey}/webinars/{webinarKey}/registrants/{registrantKey}:
    delete:
      summary: Delete registrant
      description: Removes a webinar registrant from current registrations for the
        specified webinar. The webinar must be a scheduled, future webinar.
      operationId: deleteRegistrant
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-delete
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
      - WebinarKey
      - Registrants
      - RegistrantKey
    get:
      summary: Get registrant
      description: Retrieve registration details for a specific registrant.
      operationId: getRegistrant
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-get
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
      - WebinarKey
      - Registrants
      - RegistrantKey
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions:
    get:
      summary: Get webinar sessions
      description: Retrieves details for all past sessions of a specific webinar.
      operationId: getAllSessions
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessions-get
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
      - WebinarKey
      - Sessions
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}:
    get:
      summary: Get webinar session
      description: Retrieves attendance details for a specific webinar session that
        has ended. If attendees attended the session ('registrantsAttended'), specific
        attendance details, such as attendenceTime for a registrant, will also be
        retrieved. For technical reasons, this call cannot be executed from this documentation.
        Please use the curl command to execute it.
      operationId: getWebinarSession
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkey-get
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
      - WebinarKey
      - Sessions
      - SessionKey
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/attendees:
    get:
      summary: Get session attendees
      description: Retrieve details for all attendees of a specific webinar session.
        For technical reasons, this call cannot be executed from this documentation.
        Please use the curl command to execute it.
      operationId: getAttendees
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendees-get
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
      - WebinarKey
      - Sessions
      - SessionKey
      - Attendees
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/attendees/{registrantKey}:
    get:
      summary: Get attendee
      description: Retrieve registration details for a particular attendee of a specific
        webinar session. For technical reasons, this call cannot be executed from
        this documentation. Please use the curl command to execute it.
      operationId: getAttendee
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkey-get
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
      - WebinarKey
      - Sessions
      - SessionKey
      - Attendees
      - RegistrantKey
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/attendees/{registrantKey}/polls:
    get:
      summary: Get attendee poll answers
      description: Get poll answers from a particular attendee of a specific webinar
        session. For technical reasons, this call cannot be executed from this documentation.
        Please use the curl command to execute it.
      operationId: getAttendeePollAnswers
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeypolls-get
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
      - WebinarKey
      - Sessions
      - SessionKey
      - Attendees
      - RegistrantKey
      - Polls
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/attendees/{registrantKey}/questions:
    get:
      summary: Get attendee questions
      description: Get questions asked by an attendee during a webinar session. For
        technical reasons, this call cannot be executed from this documentation. Please
        use the curl command to execute it.
      operationId: getAttendeeQuestions
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeyquestions-get
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
      - WebinarKey
      - Sessions
      - SessionKey
      - Attendees
      - RegistrantKey
      - Questions
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/attendees/{registrantKey}/surveys:
    get:
      summary: Get attendee survey answers
      description: Retrieve survey answers from a particular attendee during a webinar
        session. For technical reasons, this call cannot be executed from this documentation.
        Please use the curl command to execute it.
      operationId: getAttendeeSurveyAnswers
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeysurveys-get
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
      - WebinarKey
      - Sessions
      - SessionKey
      - Attendees
      - RegistrantKey
      - Surveys
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/performance:
    get:
      summary: Get session performance
      description: Get performance details for a session. For technical reasons, this
        call cannot be executed from this documentation. Please use the curl command
        to execute it.
      operationId: getPerformance
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyperformance-get
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
      - WebinarKey
      - Sessions
      - SessionKey
      - Performance
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/polls:
    get:
      summary: Get session polls
      description: Retrieve all collated attendee questions and answers for polls
        from a specific webinar session. For technical reasons, this call cannot be
        executed from this documentation. Please use the curl command to execute it.
      operationId: getPolls
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeypolls-get
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
      - WebinarKey
      - Sessions
      - SessionKey
      - Polls
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/questions:
    get:
      summary: Get session questions
      description: Retrieve questions and answers for a past webinar session. For
        technical reasons, this call cannot be executed from this documentation. Please
        use the curl command to execute it.
      operationId: getQuestions
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyquestions-get
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
      - WebinarKey
      - Sessions
      - SessionKey
      - Questions
  /organizers/{organizerKey}/webinars/{webinarKey}/sessions/{sessionKey}/surveys:
    get:
      summary: Get session surveys
      description: Retrieve surveys for a past webinar session. For technical reasons,
        this call cannot be executed from this documentation. Please use the curl
        command to execute it.
      operationId: getSurveys
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeysurveys-get
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
      - WebinarKey
      - Sessions
      - SessionKey
      - Surveys
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