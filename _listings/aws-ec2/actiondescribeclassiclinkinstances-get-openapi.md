---
swagger: "2.0"
x-collection-name: AWS EC2
x-complete: 0
info:
  title: AWS EC2 API Describe Classic Link Instances
  version: 1.0.0
  description: Describes one or more of your linked EC2-Classic instances.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribeClassicLinkInstances:
    get:
      summary: Describe Classic Link Instances
      description: Describes one or more of your linked EC2-Classic instances.
      operationId: describeclassiclinkinstances
      x-api-path-slug: actiondescribeclassiclinkinstances-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,     and provides an error response
        type: string
      - in: query
        name: Filter.N
        description: One or more filters
        type: string
      - in: query
        name: VpcId.N
        description: One or more VPCs for which you want to describe the ClassicLink
          status
        type: string
      responses:
        200:
          description: OK
      tags:
      - Server Instance
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