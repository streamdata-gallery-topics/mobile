---
swagger: "2.0"
x-collection-name: New Relic
x-complete: 0
info:
  title: New Relic Delete Alerts Entity Conditions Entity  . Format
  version: 1.0.0
  description: |-
    This API endpoint allows you to disassociate an entity with a specified Alerts condition.

    Note: Admin User???s API Key is required.

    Entity type options (Synthetics is not yet supported):

    BrowserApplication

    Application

    MobileApplication

    Server

    KeyTransaction

    Plugin
basePath: v2/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /mobile_applications.{format}:
    get:
      summary: Get Mobile Applications. Format
      description: |-
        This API endpoint returns a list of the Mobile Applications associated with your New Relic account.

        MobileApplications can be filtered by their name, or by the application IDs.
      operationId: getMobileApplications.Format
      x-api-path-slug: mobile-applications-format-get
      responses:
        200:
          description: OK
      tags:
      - Mobile
      - Applications.
      - Format
  /mobile_applications/{id}.{format}:
    get:
      summary: Get Mobile Applications  . Format
      description: This API endpoint returns a single Mobile Application, identified
        by ID. The time range for summary data is the last 30 minutes.
      operationId: getMobileApplications.Format
      x-api-path-slug: mobile-applicationsid-format-get
      parameters:
      - in: path
        name: id
        description: Mobile Application ID
        type: integer
      responses:
        200:
          description: OK
      tags:
      - Mobile
      - Applications
      - ""
      - .
      - Format
  /mobile_applications/{mobile_application_id}/metrics.{format}:
    get:
      summary: Get Mobile Applications Mobile Application  Metrics. Format
      description: |-
        Return a list of known metrics and their value names for the given resource.

        See our documentation for a discussion
        on  output pagination
        and for examples of requesting and using metric values.
      operationId: getMobileApplicationsMobileApplicationMetrics.Format
      x-api-path-slug: mobile-applicationsmobile-application-idmetrics-format-get
      parameters:
      - in: query
        name: cursor
        description: Cursor for next page (replacing page param)
        type: string
      - in: path
        name: mobile_application_id
        description: Mobile application ID
        type: integer
      - in: query
        name: name
        description: Filter metrics by name
        type: string
      - in: query
        name: page
        description: Pagination index (will be deprecated)
        type: integer
      responses:
        200:
          description: OK
      tags:
      - Mobile
      - Applications
      - Mobile
      - Application
      - ""
      - Metrics.
      - Format
  /mobile_applications/{mobile_application_id}/metrics/data.{format}:
    get:
      summary: Get Mobile Applications Mobile Application  Metrics Data. Format
      description: "This API endpoint returns a list of values for each of the requested
        metrics. The list of available metrics\ncan be returned using the Metric Name
        API endpoint.\n\nMetric data can be filtered by a number of parameters, including
        multiple names and values, and by time range.\nMetric names and values will
        be matched intelligently in the background.\n\nYou can also retrieve a summarized
        data point across the entire time range selected by using the summarize\nparameter.\n\nSee
        our documentation for a discussion on \noutput pagination,  time range \nrelated
        considerations, and for examples of requesting and using metric values."
      operationId: getMobileApplicationsMobileApplicationMetricsData.Format
      x-api-path-slug: mobile-applicationsmobile-application-idmetricsdata-format-get
      parameters:
      - in: query
        name: from
        description: Retrieve metrics after this time
        type: time
      - in: path
        name: mobile_application_id
        description: Mobile application ID
        type: integer
      - in: query
        name: names
        description: Retrieve specific metrics by name
        type: array
      - in: query
        name: period
        description: Period of timeslices in seconds
        type: integer
      - in: query
        name: raw
        description: Return unformatted raw values
        type: boolean
      - in: query
        name: summarize
        description: Summarize the data
        type: boolean
      - in: query
        name: to
        description: Retrieve metrics before this time
        type: time
      - in: query
        name: values
        description: Retrieve specific metric values
        type: array
      responses:
        200:
          description: OK
      tags:
      - Mobile
      - Applications
      - Mobile
      - Application
      - ""
      - Metrics
      - Data.
      - Format
  /alerts_entity_conditions/{entity_id}.{format}:
    get:
      summary: Get Alerts Entity Conditions Entity  . Format
      description: |-
        This API endpoint allows you to list the Alerts conditions an entity is part of.

        Entity type options (Synthetics is not yet supported):

        BrowserApplication

        Application

        MobileApplication

        Server

        KeyTransaction

        Plugin
      operationId: getAlertsEntityConditionsEntity.Format
      x-api-path-slug: alerts-entity-conditionsentity-id-format-get
      parameters:
      - in: path
        name: entity_id
        description: Entity ID
        type: integer
      - in: query
        name: entity_type
        description: Entity Type
        type: string
      responses:
        200:
          description: OK
      tags:
      - Alerts
      - Entity
      - Conditions
      - Entity
      - ""
      - .
      - Format
    put:
      summary: Put Alerts Entity Conditions Entity  . Format
      description: "This API endpoint allows you to add an entity to a specified Alerts
        condition.\n\nNote: Admin User???s API Key is required.\n \n  Entity type
        options (Synthetics is not yet supported):\n\nBrowserApplication\n\nApplication\n\nMobileApplication\n\nServer\n\nKeyTransaction\n\nPlugin"
      operationId: putAlertsEntityConditionsEntity.Format
      x-api-path-slug: alerts-entity-conditionsentity-id-format-put
      parameters:
      - in: query
        name: condition_id
        description: Alerts condition ID
        type: integer
      - in: path
        name: entity_id
        description: Entity id to add
        type: integer
      - in: query
        name: entity_type
        description: Entity Type
        type: string
      responses:
        200:
          description: OK
      tags:
      - Alerts
      - Entity
      - Conditions
      - Entity
      - ""
      - .
      - Format
    delete:
      summary: Delete Alerts Entity Conditions Entity  . Format
      description: |-
        This API endpoint allows you to disassociate an entity with a specified Alerts condition.

        Note: Admin User???s API Key is required.

        Entity type options (Synthetics is not yet supported):

        BrowserApplication

        Application

        MobileApplication

        Server

        KeyTransaction

        Plugin
      operationId: deleteAlertsEntityConditionsEntity.Format
      x-api-path-slug: alerts-entity-conditionsentity-id-format-delete
      parameters:
      - in: query
        name: condition_id
        description: Alerts condition ID
        type: integer
      - in: path
        name: entity_id
        description: Entity id to remove
        type: integer
      - in: query
        name: entity_type
        description: Entity Type
        type: string
      responses:
        200:
          description: OK
      tags:
      - Alerts
      - Entity
      - Conditions
      - Entity
      - ""
      - .
      - Format
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