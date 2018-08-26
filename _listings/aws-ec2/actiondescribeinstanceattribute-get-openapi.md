---
swagger: "2.0"
x-collection-name: AWS EC2
x-complete: 0
info:
  title: AWS EC2 API Describe Instance Attribute
  version: 1.0.0
  description: Describes the specified attribute of the specified instance.
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
  /?Action=ModifyInstancePlacement:
    get:
      summary: Modify Instance Placement
      description: |-
        Set the instance affinity value for a specific stopped instance and modify the
                    instance tenancy setting.
      operationId: modifyinstanceplacement
      x-api-path-slug: actionmodifyinstanceplacement-get
      parameters:
      - in: query
        name: ClientToken
        description: Unique, case-sensitive identifier you provide to ensure idempotency
          of the request
        type: string
      - in: query
        name: CurrencyCode
        description: The currency in which the totalUpfrontPrice, LimitPrice,            and
          totalHourlyPrice amounts are specified
        type: string
      - in: query
        name: HostIdSet.N
        description: The ID/s of the Dedicated Host/s that the reservation will be
          associated            with
        type: string
      - in: query
        name: LimitPrice
        description: The specified limit is checked against the total upfront cost
          of the reservation            (calculated as the offerings upfront cost
          multiplied by the host count)
        type: string
      - in: query
        name: OfferingId
        description: The ID of the offering
        type: string
      responses:
        200:
          description: OK
      tags:
      - Server Instance
  /?Action=DescribeInstanceAttribute:
    get:
      summary: Describe Instance Attribute
      description: Describes the specified attribute of the specified instance.
      operationId: describeinstanceattribute
      x-api-path-slug: actiondescribeinstanceattribute-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: Filter.N
        description: One or more filters
        type: string
      - in: query
        name: InstanceId.N
        description: One or more instance IDs
        type: string
      - in: query
        name: MaxResults
        description: The maximum number of results to return in a single call
        type: string
      - in: query
        name: NextToken
        description: The token to request the next page of results
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