---
swagger: "2.0"
info:
  title: Particle
  description: 'The Particle Cloud API is a REST API. REST means a lot of things,
    but first and foremost it means that we use the URL in the way that it''s intended:
    as a &quot;Uniform Resource Locator&quot;.In this case, the unique &quot;resource&quot;
    in question is your device (Core, Photon, Electron). Every device has a URL, which
    can be used to GET variables, POST a function call, or PUT new firmware. The variables
    and functions that you have written in your firmware are exposed as subresources
    under the device.All requests to the device come through our API server using
    TLS security.'
  version: 1.0.0
host: api.particle.io
basePath: v1/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /oauth/token:
    post:
      summary: Add Oauth Token
      description: Creates an access token that gives you access to the Cloud API
      operationId: postOauthToken
      parameters:
      - in: formData
        name: expires_at
        description: When should the token expire? This should be an ISO8601 formatted
          date string
      - in: formData
        name: expires_in
        description: How many seconds the token will be valid for
      - in: formData
        name: grant_type
        description: OAuth grant type
      - in: formData
        name: password
        description: Your Particle account password
      - in: formData
        name: username
        description: Your Particle account username
      responses:
        200:
          description: OK
      tags:
      - oauth
      - token
definitions:
  AccessTokenInfo:
    properties:
      expires_at:
        description: This is a default description.
        type: delete
      client:
        description: This is a default description.
        type: delete
  DeviceInfo:
    properties:
      name:
        description: This is a default description.
        type: delete
      last_app:
        description: This is a default description.
        type: delete
      last_ip_address:
        description: This is a default description.
        type: delete
      last_heard:
        description: This is a default description.
        type: delete
      connected:
        description: This is a default description.
        type: delete
      last_iccid:
        description: This is a default description.
        type: delete
      imei:
        description: This is a default description.
        type: delete
x-collection-name: Particle
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