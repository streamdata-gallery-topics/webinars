---
name: GoToMeeting
x-slug: gotomeeting
description: Citrix enables business mobility through the secure delivery of apps
  and data to any device on any network.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
x-kinRank: "7"
x-alexaRank: "7422"
tags: Webinars
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/apis.md
specificationVersion: "0.14"
apis:
- name: Go To Webinar - Get all webinars for an account
  x-api-slug: accountsaccountkeywebinars-get
  description: Retrieves the list of webinars for an account within a given date range.
    __*Page*__ and __*size*__ parameters are optional. Default __*page*__ is 0 and
    default __*size*__ is 20. For technical reasons, this call cannot be executed
    from this documentation. Please use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/accountsaccountkeywebinars-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/accountsaccountkeywebinars-get-openapi.md
- name: Go To Webinar - Get all webinars
  x-api-slug: organizersorganizerkeywebinars-get
  description: Returns webinars scheduled for the future for a specified organizer.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinars-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinars-get-openapi.md
- name: Go To Webinar - Create webinar
  x-api-slug: organizersorganizerkeywebinars-post
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinars-post-openapi.md
- name: Go To Webinar - Cancel webinar
  x-api-slug: organizersorganizerkeywebinarswebinarkey-delete
  description: Cancels a specific webinar. If the webinar is a series or sequence,
    this call deletes all scheduled sessions. To send cancellation emails to registrants
    set sendCancellationEmails=true in the request. When the cancellation emails are
    sent, the default generated message is used in the cancellation email body.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkey-delete-openapi.md
- name: Go To Webinar - Get webinar
  x-api-slug: organizersorganizerkeywebinarswebinarkey-get
  description: Retrieve information on a specific webinar. If the type of the webinar
    is 'sequence', a sequence of future times will be provided. Webinars of type 'series'
    are treated the same as normal webinars - each session in the webinar series has
    a different webinarKey. If an organizer cancels a webinar, then a request to get
    that webinar would return a '404 Not Found' error.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkey-get-openapi.md
- name: Go To Webinar - Update webinar
  x-api-slug: organizersorganizerkeywebinarswebinarkey-put
  description: Updates a webinar. The call requires at least one of the parameters
    in the request body. The request completely replaces the existing session, series,
    or sequence and so must include the full definition of each as for the Create
    call. Set notifyParticipants=true to send update emails to registrants.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkey-put-openapi.md
- name: Go To Webinar - Get attendees for all webinar sessions
  x-api-slug: organizersorganizerkeywebinarswebinarkeyattendees-get
  description: Returns all attendees for all sessions of the specified webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyattendees-get-openapi.md
- name: Go To Webinar - Get audio information
  x-api-slug: organizersorganizerkeywebinarswebinarkeyaudio-get
  description: Retrieves the audio/conferencing information for a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyaudio-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyaudio-get-openapi.md
- name: Go To Webinar - Update audio information
  x-api-slug: organizersorganizerkeywebinarswebinarkeyaudio-post
  description: Updates the audio/conferencing settings for a specific webinar
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyaudio-post-openapi.md
- name: Go To Webinar - Get co-organizers
  x-api-slug: organizersorganizerkeywebinarswebinarkeycoorganizers-get
  description: Returns the co-organizers for the specified webinar. The original organizer
    who created the webinar is filtered out of the list. If the webinar has no co-organizers,
    an empty array is returned. Co-organizers that do not have a GoToWebinar account
    are returned as external co-organizers. For those organizers no surname is returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeycoorganizers-get-openapi.md
- name: Go To Webinar - Create co-organizers
  x-api-slug: organizersorganizerkeywebinarswebinarkeycoorganizers-post
  description: Creates co-organizers for the specified webinar. For co-organizers
    that have a GoToWebinar account you have to set the parameter 'external' to 'false'.
    In this case you have to pass the parameter 'organizerKey' only. For co-organizers
    that have no GoToWebinar account you have to set the parameter 'external' to 'true'.
    In this case you have to pass the parameters 'givenName' and 'email'. Since there
    is no parameter for 'surname' you should pass first and last name to the parameter
    'givenName'.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeycoorganizers-post-openapi.md
- name: Go To Webinar - Delete co-organizer
  x-api-slug: organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkey-delete
  description: Deletes an internal co-organizer specified by the coorganizerKey (memberKey).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkey-delete-openapi.md
- name: Go To Webinar - Resend invitation
  x-api-slug: organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkeyresendinvitation-post
  description: Resends an invitation email to the specified co-organizer
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkeyresendinvitation-post-openapi.md
- name: Go To Webinar - Get webinar meeting times
  x-api-slug: organizersorganizerkeywebinarswebinarkeymeetingtimes-get
  description: Retrieves the meeting times for a webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeymeetingtimes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeymeetingtimes-get-openapi.md
- name: Go To Webinar - Get webinar panelists
  x-api-slug: organizersorganizerkeywebinarswebinarkeypanelists-get
  description: Retrieves all the panelists for a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelists-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelists-get-openapi.md
- name: Go To Webinar - Create Panelists
  x-api-slug: organizersorganizerkeywebinarswebinarkeypanelists-post
  description: Create panelists for a specified webinar
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelists-post-openapi.md
- name: Go To Webinar - Delete webinar panelist
  x-api-slug: organizersorganizerkeywebinarswebinarkeypanelistspanelistkey-delete
  description: Removes a webinar panelist.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelistspanelistkey-delete-openapi.md
- name: Go To Webinar - Resend panelist invitation
  x-api-slug: organizersorganizerkeywebinarswebinarkeypanelistspanelistkeyresendinvitation-post
  description: Resend the panelist invitation email.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelistspanelistkeyresendinvitation-post-openapi.md
- name: Go To Webinar - Get performance for all webinar sessions
  x-api-slug: organizersorganizerkeywebinarswebinarkeyperformance-get
  description: Gets performance details for all sessions of a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyperformance-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyperformance-get-openapi.md
- name: Go To Webinar - Get registrants
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrants-get
  description: Retrieve registration details for all registrants of a specific webinar.
    Registrant details will not include all fields captured when creating the registrant.
    To see all data, use the API call 'Get Registrant'. Registrants can have one of
    the following states; <br>WAITING - registrant registered and is awaiting approval
    (where organizer has required approval), <br>APPROVED - registrant registered
    and is approved, and <br>DENIED - registrant registered and was denied.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrants-get-openapi.md
- name: Go To Webinar - Create registrant
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrants-post
  description: 'Register an attendee for a scheduled webinar. The response contains
    the registrantKey and join URL for the registrant. An email will be sent to the
    registrant unless the organizer turns off the confirmation email setting from
    the GoToWebinar website. Please note that you must provide all required fields
    including custom fields defined during the webinar creation. Use the API call
    ''Get registration fields'' to get a list of all fields, if they are required,
    and their possible values. At this time there are two versions of the ''Create
    Registrant'' call. The first version only accepts firstName, lastName, and email
    and ignores all other fields. If you have custom fields or want to capture additional
    information this version won''t work for you. The second version allows you to
    pass all required and optional fields, including custom fields defined when creating
    the webinar. To use the second version you must pass the header value ''Accept:
    application/vnd.citrix.g2wapi-v1.1+json'' instead of ''Accept: application/json''.
    Leaving this header out results in the first version of the API call.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrants-post-openapi.md
- name: Go To Webinar - Get registration fields
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrantsfields-get
  description: Retrieve required, optional registration, and custom questions for
    a specified webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrantsfields-get-openapi.md
- name: Go To Webinar - Delete registrant
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-delete
  description: Removes a webinar registrant from current registrations for the specified
    webinar. The webinar must be a scheduled, future webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-delete-openapi.md
- name: Go To Webinar - Get registrant
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-get
  description: Retrieve registration details for a specific registrant.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-get-openapi.md
- name: Go To Webinar - Get webinar sessions
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessions-get
  description: Retrieves details for all past sessions of a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessions-get-openapi.md
- name: Go To Webinar - Get webinar session
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkey-get
  description: Retrieves attendance details for a specific webinar session that has
    ended. If attendees attended the session ('registrantsAttended'), specific attendance
    details, such as attendenceTime for a registrant, will also be retrieved. For
    technical reasons, this call cannot be executed from this documentation. Please
    use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkey-get-openapi.md
- name: Go To Webinar - Get session attendees
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendees-get
  description: Retrieve details for all attendees of a specific webinar session. For
    technical reasons, this call cannot be executed from this documentation. Please
    use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendees-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendees-get-openapi.md
- name: Go To Webinar - Get attendee
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkey-get
  description: Retrieve registration details for a particular attendee of a specific
    webinar session. For technical reasons, this call cannot be executed from this
    documentation. Please use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkey-get-openapi.md
- name: Go To Webinar - Get attendee poll answers
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeypolls-get
  description: Get poll answers from a particular attendee of a specific webinar session.
    For technical reasons, this call cannot be executed from this documentation. Please
    use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeypolls-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeypolls-get-openapi.md
- name: Go To Webinar - Get attendee questions
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeyquestions-get
  description: Get questions asked by an attendee during a webinar session. For technical
    reasons, this call cannot be executed from this documentation. Please use the
    curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeyquestions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeyquestions-get-openapi.md
- name: Go To Webinar - Get attendee survey answers
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeysurveys-get
  description: Retrieve survey answers from a particular attendee during a webinar
    session. For technical reasons, this call cannot be executed from this documentation.
    Please use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeysurveys-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeysurveys-get-openapi.md
- name: Go To Webinar - Get session performance
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyperformance-get
  description: Get performance details for a session. For technical reasons, this
    call cannot be executed from this documentation. Please use the curl command to
    execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyperformance-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyperformance-get-openapi.md
- name: Go To Webinar - Get session polls
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeypolls-get
  description: Retrieve all collated attendee questions and answers for polls from
    a specific webinar session. For technical reasons, this call cannot be executed
    from this documentation. Please use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeypolls-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeypolls-get-openapi.md
- name: Go To Webinar - Get session questions
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyquestions-get
  description: Retrieve questions and answers for a past webinar session. For technical
    reasons, this call cannot be executed from this documentation. Please use the
    curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyquestions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyquestions-get-openapi.md
- name: Go To Webinar - Get session surveys
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeysurveys-get
  description: Retrieve surveys for a past webinar session. For technical reasons,
    this call cannot be executed from this documentation. Please use the curl command
    to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeysurveys-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeysurveys-get-openapi.md
- name: Go To Webinar - Cancel webinar
  x-api-slug: organizersorganizerkeywebinarswebinarkey-delete
  description: Cancels a specific webinar. If the webinar is a series or sequence,
    this call deletes all scheduled sessions. To send cancellation emails to registrants
    set sendCancellationEmails=true in the request. When the cancellation emails are
    sent, the default generated message is used in the cancellation email body.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkey-delete-openapi.md
- name: Go To Webinar - Get webinar
  x-api-slug: organizersorganizerkeywebinarswebinarkey-get
  description: Retrieve information on a specific webinar. If the type of the webinar
    is 'sequence', a sequence of future times will be provided. Webinars of type 'series'
    are treated the same as normal webinars - each session in the webinar series has
    a different webinarKey. If an organizer cancels a webinar, then a request to get
    that webinar would return a '404 Not Found' error.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkey-get-openapi.md
- name: Go To Webinar - Update webinar
  x-api-slug: organizersorganizerkeywebinarswebinarkey-put
  description: Updates a webinar. The call requires at least one of the parameters
    in the request body. The request completely replaces the existing session, series,
    or sequence and so must include the full definition of each as for the Create
    call. Set notifyParticipants=true to send update emails to registrants.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkey-put-openapi.md
- name: Go To Webinar - Get attendees for all webinar sessions
  x-api-slug: organizersorganizerkeywebinarswebinarkeyattendees-get
  description: Returns all attendees for all sessions of the specified webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyattendees-get-openapi.md
- name: Go To Webinar - Get audio information
  x-api-slug: organizersorganizerkeywebinarswebinarkeyaudio-get
  description: Retrieves the audio/conferencing information for a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyaudio-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyaudio-get-openapi.md
- name: Go To Webinar - Update audio information
  x-api-slug: organizersorganizerkeywebinarswebinarkeyaudio-post
  description: Updates the audio/conferencing settings for a specific webinar
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyaudio-post-openapi.md
- name: Go To Webinar - Get co-organizers
  x-api-slug: organizersorganizerkeywebinarswebinarkeycoorganizers-get
  description: Returns the co-organizers for the specified webinar. The original organizer
    who created the webinar is filtered out of the list. If the webinar has no co-organizers,
    an empty array is returned. Co-organizers that do not have a GoToWebinar account
    are returned as external co-organizers. For those organizers no surname is returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeycoorganizers-get-openapi.md
- name: Go To Webinar - Create co-organizers
  x-api-slug: organizersorganizerkeywebinarswebinarkeycoorganizers-post
  description: Creates co-organizers for the specified webinar. For co-organizers
    that have a GoToWebinar account you have to set the parameter 'external' to 'false'.
    In this case you have to pass the parameter 'organizerKey' only. For co-organizers
    that have no GoToWebinar account you have to set the parameter 'external' to 'true'.
    In this case you have to pass the parameters 'givenName' and 'email'. Since there
    is no parameter for 'surname' you should pass first and last name to the parameter
    'givenName'.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeycoorganizers-post-openapi.md
- name: Go To Webinar - Delete co-organizer
  x-api-slug: organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkey-delete
  description: Deletes an internal co-organizer specified by the coorganizerKey (memberKey).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkey-delete-openapi.md
- name: Go To Webinar - Resend invitation
  x-api-slug: organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkeyresendinvitation-post
  description: Resends an invitation email to the specified co-organizer
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkeyresendinvitation-post-openapi.md
- name: Go To Webinar - Get webinar meeting times
  x-api-slug: organizersorganizerkeywebinarswebinarkeymeetingtimes-get
  description: Retrieves the meeting times for a webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeymeetingtimes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeymeetingtimes-get-openapi.md
- name: Go To Webinar - Get webinar panelists
  x-api-slug: organizersorganizerkeywebinarswebinarkeypanelists-get
  description: Retrieves all the panelists for a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelists-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelists-get-openapi.md
- name: Go To Webinar - Create Panelists
  x-api-slug: organizersorganizerkeywebinarswebinarkeypanelists-post
  description: Create panelists for a specified webinar
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelists-post-openapi.md
- name: Go To Webinar - Delete webinar panelist
  x-api-slug: organizersorganizerkeywebinarswebinarkeypanelistspanelistkey-delete
  description: Removes a webinar panelist.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelistspanelistkey-delete-openapi.md
- name: Go To Webinar - Resend panelist invitation
  x-api-slug: organizersorganizerkeywebinarswebinarkeypanelistspanelistkeyresendinvitation-post
  description: Resend the panelist invitation email.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelistspanelistkeyresendinvitation-post-openapi.md
- name: Go To Webinar - Get performance for all webinar sessions
  x-api-slug: organizersorganizerkeywebinarswebinarkeyperformance-get
  description: Gets performance details for all sessions of a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyperformance-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyperformance-get-openapi.md
- name: Go To Webinar - Get registrants
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrants-get
  description: Retrieve registration details for all registrants of a specific webinar.
    Registrant details will not include all fields captured when creating the registrant.
    To see all data, use the API call 'Get Registrant'. Registrants can have one of
    the following states; <br>WAITING - registrant registered and is awaiting approval
    (where organizer has required approval), <br>APPROVED - registrant registered
    and is approved, and <br>DENIED - registrant registered and was denied.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrants-get-openapi.md
- name: Go To Webinar - Create registrant
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrants-post
  description: 'Register an attendee for a scheduled webinar. The response contains
    the registrantKey and join URL for the registrant. An email will be sent to the
    registrant unless the organizer turns off the confirmation email setting from
    the GoToWebinar website. Please note that you must provide all required fields
    including custom fields defined during the webinar creation. Use the API call
    ''Get registration fields'' to get a list of all fields, if they are required,
    and their possible values. At this time there are two versions of the ''Create
    Registrant'' call. The first version only accepts firstName, lastName, and email
    and ignores all other fields. If you have custom fields or want to capture additional
    information this version won''t work for you. The second version allows you to
    pass all required and optional fields, including custom fields defined when creating
    the webinar. To use the second version you must pass the header value ''Accept:
    application/vnd.citrix.g2wapi-v1.1+json'' instead of ''Accept: application/json''.
    Leaving this header out results in the first version of the API call.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrants-post-openapi.md
- name: Go To Webinar - Get registration fields
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrantsfields-get
  description: Retrieve required, optional registration, and custom questions for
    a specified webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrantsfields-get-openapi.md
- name: Go To Webinar - Delete registrant
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-delete
  description: Removes a webinar registrant from current registrations for the specified
    webinar. The webinar must be a scheduled, future webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-delete-openapi.md
- name: Go To Webinar - Get registrant
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-get
  description: Retrieve registration details for a specific registrant.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-get-openapi.md
- name: Go To Webinar - Get webinar sessions
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessions-get
  description: Retrieves details for all past sessions of a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessions-get-openapi.md
- name: Go To Webinar - Get webinar session
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkey-get
  description: Retrieves attendance details for a specific webinar session that has
    ended. If attendees attended the session ('registrantsAttended'), specific attendance
    details, such as attendenceTime for a registrant, will also be retrieved. For
    technical reasons, this call cannot be executed from this documentation. Please
    use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkey-get-openapi.md
- name: Go To Webinar - Get session attendees
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendees-get
  description: Retrieve details for all attendees of a specific webinar session. For
    technical reasons, this call cannot be executed from this documentation. Please
    use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendees-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendees-get-openapi.md
- name: Go To Webinar - Get attendee
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkey-get
  description: Retrieve registration details for a particular attendee of a specific
    webinar session. For technical reasons, this call cannot be executed from this
    documentation. Please use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkey-get-openapi.md
- name: Go To Webinar - Get attendee poll answers
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeypolls-get
  description: Get poll answers from a particular attendee of a specific webinar session.
    For technical reasons, this call cannot be executed from this documentation. Please
    use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeypolls-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeypolls-get-openapi.md
- name: Go To Webinar - Get attendee questions
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeyquestions-get
  description: Get questions asked by an attendee during a webinar session. For technical
    reasons, this call cannot be executed from this documentation. Please use the
    curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeyquestions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeyquestions-get-openapi.md
- name: Go To Webinar - Get attendee survey answers
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeysurveys-get
  description: Retrieve survey answers from a particular attendee during a webinar
    session. For technical reasons, this call cannot be executed from this documentation.
    Please use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeysurveys-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeysurveys-get-openapi.md
- name: Go To Webinar - Get session performance
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyperformance-get
  description: Get performance details for a session. For technical reasons, this
    call cannot be executed from this documentation. Please use the curl command to
    execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyperformance-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyperformance-get-openapi.md
- name: Go To Webinar - Get session polls
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeypolls-get
  description: Retrieve all collated attendee questions and answers for polls from
    a specific webinar session. For technical reasons, this call cannot be executed
    from this documentation. Please use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeypolls-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeypolls-get-openapi.md
- name: Go To Webinar - Get session questions
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyquestions-get
  description: Retrieve questions and answers for a past webinar session. For technical
    reasons, this call cannot be executed from this documentation. Please use the
    curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyquestions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyquestions-get-openapi.md
- name: Go To Webinar - Get session surveys
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeysurveys-get
  description: Retrieve surveys for a past webinar session. For technical reasons,
    this call cannot be executed from this documentation. Please use the curl command
    to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeysurveys-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeysurveys-get-openapi.md
- name: Go To Webinar - Cancel webinar
  x-api-slug: organizersorganizerkeywebinarswebinarkey-delete
  description: Cancels a specific webinar. If the webinar is a series or sequence,
    this call deletes all scheduled sessions. To send cancellation emails to registrants
    set sendCancellationEmails=true in the request. When the cancellation emails are
    sent, the default generated message is used in the cancellation email body.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkey-delete-openapi.md
- name: Go To Webinar - Get webinar
  x-api-slug: organizersorganizerkeywebinarswebinarkey-get
  description: Retrieve information on a specific webinar. If the type of the webinar
    is 'sequence', a sequence of future times will be provided. Webinars of type 'series'
    are treated the same as normal webinars - each session in the webinar series has
    a different webinarKey. If an organizer cancels a webinar, then a request to get
    that webinar would return a '404 Not Found' error.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkey-get-openapi.md
- name: Go To Webinar - Update webinar
  x-api-slug: organizersorganizerkeywebinarswebinarkey-put
  description: Updates a webinar. The call requires at least one of the parameters
    in the request body. The request completely replaces the existing session, series,
    or sequence and so must include the full definition of each as for the Create
    call. Set notifyParticipants=true to send update emails to registrants.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkey-put-openapi.md
- name: Go To Webinar - Get attendees for all webinar sessions
  x-api-slug: organizersorganizerkeywebinarswebinarkeyattendees-get
  description: Returns all attendees for all sessions of the specified webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyattendees-get-openapi.md
- name: Go To Webinar - Get audio information
  x-api-slug: organizersorganizerkeywebinarswebinarkeyaudio-get
  description: Retrieves the audio/conferencing information for a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyaudio-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyaudio-get-openapi.md
- name: Go To Webinar - Update audio information
  x-api-slug: organizersorganizerkeywebinarswebinarkeyaudio-post
  description: Updates the audio/conferencing settings for a specific webinar
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyaudio-post-openapi.md
- name: Go To Webinar - Get co-organizers
  x-api-slug: organizersorganizerkeywebinarswebinarkeycoorganizers-get
  description: Returns the co-organizers for the specified webinar. The original organizer
    who created the webinar is filtered out of the list. If the webinar has no co-organizers,
    an empty array is returned. Co-organizers that do not have a GoToWebinar account
    are returned as external co-organizers. For those organizers no surname is returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeycoorganizers-get-openapi.md
- name: Go To Webinar - Create co-organizers
  x-api-slug: organizersorganizerkeywebinarswebinarkeycoorganizers-post
  description: Creates co-organizers for the specified webinar. For co-organizers
    that have a GoToWebinar account you have to set the parameter 'external' to 'false'.
    In this case you have to pass the parameter 'organizerKey' only. For co-organizers
    that have no GoToWebinar account you have to set the parameter 'external' to 'true'.
    In this case you have to pass the parameters 'givenName' and 'email'. Since there
    is no parameter for 'surname' you should pass first and last name to the parameter
    'givenName'.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeycoorganizers-post-openapi.md
- name: Go To Webinar - Delete co-organizer
  x-api-slug: organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkey-delete
  description: Deletes an internal co-organizer specified by the coorganizerKey (memberKey).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkey-delete-openapi.md
- name: Go To Webinar - Resend invitation
  x-api-slug: organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkeyresendinvitation-post
  description: Resends an invitation email to the specified co-organizer
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkeyresendinvitation-post-openapi.md
- name: Go To Webinar - Get webinar meeting times
  x-api-slug: organizersorganizerkeywebinarswebinarkeymeetingtimes-get
  description: Retrieves the meeting times for a webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeymeetingtimes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeymeetingtimes-get-openapi.md
- name: Go To Webinar - Get webinar panelists
  x-api-slug: organizersorganizerkeywebinarswebinarkeypanelists-get
  description: Retrieves all the panelists for a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelists-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelists-get-openapi.md
- name: Go To Webinar - Create Panelists
  x-api-slug: organizersorganizerkeywebinarswebinarkeypanelists-post
  description: Create panelists for a specified webinar
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelists-post-openapi.md
- name: Go To Webinar - Delete webinar panelist
  x-api-slug: organizersorganizerkeywebinarswebinarkeypanelistspanelistkey-delete
  description: Removes a webinar panelist.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelistspanelistkey-delete-openapi.md
- name: Go To Webinar - Resend panelist invitation
  x-api-slug: organizersorganizerkeywebinarswebinarkeypanelistspanelistkeyresendinvitation-post
  description: Resend the panelist invitation email.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelistspanelistkeyresendinvitation-post-openapi.md
- name: Go To Webinar - Get performance for all webinar sessions
  x-api-slug: organizersorganizerkeywebinarswebinarkeyperformance-get
  description: Gets performance details for all sessions of a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyperformance-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyperformance-get-openapi.md
- name: Go To Webinar - Get registrants
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrants-get
  description: Retrieve registration details for all registrants of a specific webinar.
    Registrant details will not include all fields captured when creating the registrant.
    To see all data, use the API call 'Get Registrant'. Registrants can have one of
    the following states; <br>WAITING - registrant registered and is awaiting approval
    (where organizer has required approval), <br>APPROVED - registrant registered
    and is approved, and <br>DENIED - registrant registered and was denied.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrants-get-openapi.md
- name: Go To Webinar - Create registrant
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrants-post
  description: 'Register an attendee for a scheduled webinar. The response contains
    the registrantKey and join URL for the registrant. An email will be sent to the
    registrant unless the organizer turns off the confirmation email setting from
    the GoToWebinar website. Please note that you must provide all required fields
    including custom fields defined during the webinar creation. Use the API call
    ''Get registration fields'' to get a list of all fields, if they are required,
    and their possible values. At this time there are two versions of the ''Create
    Registrant'' call. The first version only accepts firstName, lastName, and email
    and ignores all other fields. If you have custom fields or want to capture additional
    information this version won''t work for you. The second version allows you to
    pass all required and optional fields, including custom fields defined when creating
    the webinar. To use the second version you must pass the header value ''Accept:
    application/vnd.citrix.g2wapi-v1.1+json'' instead of ''Accept: application/json''.
    Leaving this header out results in the first version of the API call.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrants-post-openapi.md
- name: Go To Webinar - Get registration fields
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrantsfields-get
  description: Retrieve required, optional registration, and custom questions for
    a specified webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrantsfields-get-openapi.md
- name: Go To Webinar - Delete registrant
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-delete
  description: Removes a webinar registrant from current registrations for the specified
    webinar. The webinar must be a scheduled, future webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-delete-openapi.md
- name: Go To Webinar - Get registrant
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-get
  description: Retrieve registration details for a specific registrant.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-get-openapi.md
- name: Go To Webinar - Get webinar sessions
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessions-get
  description: Retrieves details for all past sessions of a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessions-get-openapi.md
- name: Go To Webinar - Get webinar session
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkey-get
  description: Retrieves attendance details for a specific webinar session that has
    ended. If attendees attended the session ('registrantsAttended'), specific attendance
    details, such as attendenceTime for a registrant, will also be retrieved. For
    technical reasons, this call cannot be executed from this documentation. Please
    use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkey-get-openapi.md
- name: Go To Webinar - Get session attendees
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendees-get
  description: Retrieve details for all attendees of a specific webinar session. For
    technical reasons, this call cannot be executed from this documentation. Please
    use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendees-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendees-get-openapi.md
- name: Go To Webinar - Get attendee
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkey-get
  description: Retrieve registration details for a particular attendee of a specific
    webinar session. For technical reasons, this call cannot be executed from this
    documentation. Please use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkey-get-openapi.md
- name: Go To Webinar - Get attendee poll answers
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeypolls-get
  description: Get poll answers from a particular attendee of a specific webinar session.
    For technical reasons, this call cannot be executed from this documentation. Please
    use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeypolls-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeypolls-get-openapi.md
- name: Go To Webinar - Get attendee questions
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeyquestions-get
  description: Get questions asked by an attendee during a webinar session. For technical
    reasons, this call cannot be executed from this documentation. Please use the
    curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeyquestions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeyquestions-get-openapi.md
- name: Go To Webinar - Get attendee survey answers
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeysurveys-get
  description: Retrieve survey answers from a particular attendee during a webinar
    session. For technical reasons, this call cannot be executed from this documentation.
    Please use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeysurveys-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeysurveys-get-openapi.md
- name: Go To Webinar - Get session performance
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyperformance-get
  description: Get performance details for a session. For technical reasons, this
    call cannot be executed from this documentation. Please use the curl command to
    execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyperformance-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyperformance-get-openapi.md
- name: Go To Webinar - Get session polls
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeypolls-get
  description: Retrieve all collated attendee questions and answers for polls from
    a specific webinar session. For technical reasons, this call cannot be executed
    from this documentation. Please use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeypolls-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeypolls-get-openapi.md
- name: Go To Webinar - Get session questions
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyquestions-get
  description: Retrieve questions and answers for a past webinar session. For technical
    reasons, this call cannot be executed from this documentation. Please use the
    curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyquestions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyquestions-get-openapi.md
- name: Go To Webinar - Get session surveys
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeysurveys-get
  description: Retrieve surveys for a past webinar session. For technical reasons,
    this call cannot be executed from this documentation. Please use the curl command
    to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeysurveys-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeysurveys-get-openapi.md
- name: Go To Webinar - Get session surveys
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeysurveys-get
  description: Retrieve surveys for a past webinar session. For technical reasons,
    this call cannot be executed from this documentation. Please use the curl command
    to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeysurveys-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeysurveys-get-openapi.md
- name: Go To Webinar - Get session questions
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyquestions-get
  description: Retrieve questions and answers for a past webinar session. For technical
    reasons, this call cannot be executed from this documentation. Please use the
    curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyquestions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyquestions-get-openapi.md
- name: Go To Webinar - Get session polls
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeypolls-get
  description: Retrieve all collated attendee questions and answers for polls from
    a specific webinar session. For technical reasons, this call cannot be executed
    from this documentation. Please use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeypolls-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeypolls-get-openapi.md
- name: Go To Webinar - Get session performance
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyperformance-get
  description: Get performance details for a session. For technical reasons, this
    call cannot be executed from this documentation. Please use the curl command to
    execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyperformance-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyperformance-get-openapi.md
- name: Go To Webinar - Get attendee survey answers
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeysurveys-get
  description: Retrieve survey answers from a particular attendee during a webinar
    session. For technical reasons, this call cannot be executed from this documentation.
    Please use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeysurveys-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeysurveys-get-openapi.md
- name: Go To Webinar - Get attendee questions
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeyquestions-get
  description: Get questions asked by an attendee during a webinar session. For technical
    reasons, this call cannot be executed from this documentation. Please use the
    curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeyquestions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeyquestions-get-openapi.md
- name: Go To Webinar - Get attendee poll answers
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeypolls-get
  description: Get poll answers from a particular attendee of a specific webinar session.
    For technical reasons, this call cannot be executed from this documentation. Please
    use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeypolls-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeypolls-get-openapi.md
- name: Go To Webinar - Get attendee
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkey-get
  description: Retrieve registration details for a particular attendee of a specific
    webinar session. For technical reasons, this call cannot be executed from this
    documentation. Please use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkey-get-openapi.md
- name: Go To Webinar - Get session attendees
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendees-get
  description: Retrieve details for all attendees of a specific webinar session. For
    technical reasons, this call cannot be executed from this documentation. Please
    use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendees-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendees-get-openapi.md
- name: Go To Webinar - Get webinar session
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkey-get
  description: Retrieves attendance details for a specific webinar session that has
    ended. If attendees attended the session ('registrantsAttended'), specific attendance
    details, such as attendenceTime for a registrant, will also be retrieved. For
    technical reasons, this call cannot be executed from this documentation. Please
    use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkey-get-openapi.md
- name: Go To Webinar - Get webinar sessions
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessions-get
  description: Retrieves details for all past sessions of a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessions-get-openapi.md
- name: Go To Webinar - Get registrant
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-get
  description: Retrieve registration details for a specific registrant.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-get-openapi.md
- name: Go To Webinar - Delete registrant
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-delete
  description: Removes a webinar registrant from current registrations for the specified
    webinar. The webinar must be a scheduled, future webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-delete-openapi.md
- name: Go To Webinar - Get registration fields
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrantsfields-get
  description: Retrieve required, optional registration, and custom questions for
    a specified webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrantsfields-get-openapi.md
- name: Go To Webinar - Create registrant
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrants-post
  description: 'Register an attendee for a scheduled webinar. The response contains
    the registrantKey and join URL for the registrant. An email will be sent to the
    registrant unless the organizer turns off the confirmation email setting from
    the GoToWebinar website. Please note that you must provide all required fields
    including custom fields defined during the webinar creation. Use the API call
    ''Get registration fields'' to get a list of all fields, if they are required,
    and their possible values. At this time there are two versions of the ''Create
    Registrant'' call. The first version only accepts firstName, lastName, and email
    and ignores all other fields. If you have custom fields or want to capture additional
    information this version won''t work for you. The second version allows you to
    pass all required and optional fields, including custom fields defined when creating
    the webinar. To use the second version you must pass the header value ''Accept:
    application/vnd.citrix.g2wapi-v1.1+json'' instead of ''Accept: application/json''.
    Leaving this header out results in the first version of the API call.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrants-post-openapi.md
- name: Go To Webinar - Get registrants
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrants-get
  description: Retrieve registration details for all registrants of a specific webinar.
    Registrant details will not include all fields captured when creating the registrant.
    To see all data, use the API call 'Get Registrant'. Registrants can have one of
    the following states; <br>WAITING - registrant registered and is awaiting approval
    (where organizer has required approval), <br>APPROVED - registrant registered
    and is approved, and <br>DENIED - registrant registered and was denied.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrants-get-openapi.md
- name: Go To Webinar - Get performance for all webinar sessions
  x-api-slug: organizersorganizerkeywebinarswebinarkeyperformance-get
  description: Gets performance details for all sessions of a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyperformance-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyperformance-get-openapi.md
- name: Go To Webinar - Resend panelist invitation
  x-api-slug: organizersorganizerkeywebinarswebinarkeypanelistspanelistkeyresendinvitation-post
  description: Resend the panelist invitation email.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelistspanelistkeyresendinvitation-post-openapi.md
- name: Go To Webinar - Delete webinar panelist
  x-api-slug: organizersorganizerkeywebinarswebinarkeypanelistspanelistkey-delete
  description: Removes a webinar panelist.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelistspanelistkey-delete-openapi.md
- name: Go To Webinar - Create Panelists
  x-api-slug: organizersorganizerkeywebinarswebinarkeypanelists-post
  description: Create panelists for a specified webinar
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelists-post-openapi.md
- name: Go To Webinar - Get webinar panelists
  x-api-slug: organizersorganizerkeywebinarswebinarkeypanelists-get
  description: Retrieves all the panelists for a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelists-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelists-get-openapi.md
- name: Go To Webinar - Get webinar meeting times
  x-api-slug: organizersorganizerkeywebinarswebinarkeymeetingtimes-get
  description: Retrieves the meeting times for a webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeymeetingtimes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeymeetingtimes-get-openapi.md
- name: Go To Webinar - Resend invitation
  x-api-slug: organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkeyresendinvitation-post
  description: Resends an invitation email to the specified co-organizer
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkeyresendinvitation-post-openapi.md
- name: Go To Webinar - Delete co-organizer
  x-api-slug: organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkey-delete
  description: Deletes an internal co-organizer specified by the coorganizerKey (memberKey).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkey-delete-openapi.md
- name: Go To Webinar - Create co-organizers
  x-api-slug: organizersorganizerkeywebinarswebinarkeycoorganizers-post
  description: Creates co-organizers for the specified webinar. For co-organizers
    that have a GoToWebinar account you have to set the parameter 'external' to 'false'.
    In this case you have to pass the parameter 'organizerKey' only. For co-organizers
    that have no GoToWebinar account you have to set the parameter 'external' to 'true'.
    In this case you have to pass the parameters 'givenName' and 'email'. Since there
    is no parameter for 'surname' you should pass first and last name to the parameter
    'givenName'.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeycoorganizers-post-openapi.md
- name: Go To Webinar - Get co-organizers
  x-api-slug: organizersorganizerkeywebinarswebinarkeycoorganizers-get
  description: Returns the co-organizers for the specified webinar. The original organizer
    who created the webinar is filtered out of the list. If the webinar has no co-organizers,
    an empty array is returned. Co-organizers that do not have a GoToWebinar account
    are returned as external co-organizers. For those organizers no surname is returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeycoorganizers-get-openapi.md
- name: Go To Webinar - Update audio information
  x-api-slug: organizersorganizerkeywebinarswebinarkeyaudio-post
  description: Updates the audio/conferencing settings for a specific webinar
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyaudio-post-openapi.md
- name: Go To Webinar - Get audio information
  x-api-slug: organizersorganizerkeywebinarswebinarkeyaudio-get
  description: Retrieves the audio/conferencing information for a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyaudio-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyaudio-get-openapi.md
- name: Go To Webinar - Get attendees for all webinar sessions
  x-api-slug: organizersorganizerkeywebinarswebinarkeyattendees-get
  description: Returns all attendees for all sessions of the specified webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyattendees-get-openapi.md
- name: Go To Webinar - Update webinar
  x-api-slug: organizersorganizerkeywebinarswebinarkey-put
  description: Updates a webinar. The call requires at least one of the parameters
    in the request body. The request completely replaces the existing session, series,
    or sequence and so must include the full definition of each as for the Create
    call. Set notifyParticipants=true to send update emails to registrants.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkey-put-openapi.md
- name: Go To Webinar - Get webinar
  x-api-slug: organizersorganizerkeywebinarswebinarkey-get
  description: Retrieve information on a specific webinar. If the type of the webinar
    is 'sequence', a sequence of future times will be provided. Webinars of type 'series'
    are treated the same as normal webinars - each session in the webinar series has
    a different webinarKey. If an organizer cancels a webinar, then a request to get
    that webinar would return a '404 Not Found' error.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkey-get-openapi.md
- name: Go To Webinar - Cancel webinar
  x-api-slug: organizersorganizerkeywebinarswebinarkey-delete
  description: Cancels a specific webinar. If the webinar is a series or sequence,
    this call deletes all scheduled sessions. To send cancellation emails to registrants
    set sendCancellationEmails=true in the request. When the cancellation emails are
    sent, the default generated message is used in the cancellation email body.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/webinars/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkey-delete-openapi.md
x-common:
- type: x-api-gallery
  url: http://google.url.shortener.api.gallery.streamdata.io
- type: x-api-stack
  url: http://gotomeeting.stack.network
- type: x-base
  url: https://api.citrixonline.com
- type: x-blog
  url: http://blogs.citrix.com/
- type: x-crunchbase
  url: https://crunchbase.com/organization/citrix-systems
- type: x-crunchbase
  url: http://www.crunchbase.com/company/citrix-systems
- type: x-developer
  url: https://developer.citrixonline.com/
- type: x-email
  url: secure@citrix.com
- type: x-email
  url: americasconsulting@citrix.com
- type: x-email
  url: poland@citrix.com
- type: x-email
  url: citrix_ru@citrix.com
- type: x-email
  url: Licensing-emea@eu.citrix.com
- type: x-email
  url: eduardo.fleites@citrix.com
- type: x-email
  url: CitrixReady@citrix.com
- type: x-email
  url: CSP@citrix.com
- type: x-email
  url: partneroperationsEMEA@eu.citrix.com
- type: x-github
  url: https://github.com/citrix
- type: x-twitter
  url: https://twitter.com/gotomeeting
- type: x-twitter
  url: https://twitter.com/citrix
- type: x-website
  url: https://citrixonline.com
- type: x-website
  url: http://citrixonline.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---