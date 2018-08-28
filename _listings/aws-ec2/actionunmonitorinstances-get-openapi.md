---
swagger: "2.0"
x-collection-name: AWS EC2
x-complete: 0
info:
  title: AWS EC2 API Unmonitor Instances
  version: 1.0.0
  description: Disables detailed monitoring for a running instance.
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
  /?Action=DescribeInstances:
    get:
      summary: Describe Instances
      description: Describes one or more of your instances.
      operationId: describeinstances
      x-api-path-slug: actiondescribeinstances-get
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
        name: IncludeAllInstances
        description: When true, includes the health status for all instances
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
        description: The token to retrieve the next page of results
        type: string
      responses:
        200:
          description: OK
      tags:
      - Server Instance
  /?Action=ModifyInstanceAttribute:
    get:
      summary: Modify Instance Attribute
      description: Modifies the specified attribute of the specified instance.
      operationId: modifyinstanceattribute
      x-api-path-slug: actionmodifyinstanceattribute-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: InstanceId.N
        description: One or more instance IDs
        type: string
      responses:
        200:
          description: OK
      tags:
      - Server Instance
  /?Action=ReportInstanceStatus:
    get:
      summary: Report Instance Status
      description: Submits feedback about the status of an instance.
      operationId: reportinstancestatus
      x-api-path-slug: actionreportinstancestatus-get
      parameters:
      - in: query
        name: Attribute
        description: The attribute to reset
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: InstanceId
        description: The ID of the instance
        type: string
      responses:
        200:
          description: OK
      tags:
      - Server Instance
  /?Action=ResetInstanceAttribute:
    get:
      summary: Reset Instance Attribute
      description: Resets an attribute of an instance to its default value.
      operationId: resetinstanceattribute
      x-api-path-slug: actionresetinstanceattribute-get
      parameters:
      - in: query
        name: AdditionalInfo
        description: Reserved
        type: string
      - in: query
        name: BlockDeviceMapping.N
        description: The block device mapping
        type: string
      - in: query
        name: ClientToken
        description: Unique, case-sensitive identifier you provide to ensure the idempotency
          of the request
        type: string
      - in: query
        name: DisableApiTermination
        description: If you set this parameter to true, you cant terminate the instance            using
          the Amazon EC2 console, CLI, or API; otherwise, you can
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: EbsOptimized
        description: Indicates whether the instance is optimized for EBS I/O
        type: string
      - in: query
        name: IamInstanceProfile
        description: The IAM instance profile
        type: string
      - in: query
        name: ImageId
        description: The ID of the AMI, which you can get by calling DescribeImages
        type: string
      - in: query
        name: InstanceInitiatedShutdownBehavior
        description: Indicates whether an instance stops or terminates when you initiate
          shutdown from the instance (using the operating system command for system
          shutdown)
        type: string
      - in: query
        name: InstanceType
        description: The instance type
        type: string
      - in: query
        name: Ipv6Address.N
        description: '[EC2-VPC] Specify one or more IPv6 addresses from the range
          of the subnet to            associate with the primary network interface'
        type: string
      - in: query
        name: Ipv6AddressCount
        description: '[EC2-VPC] A number of IPv6 addresses to associate with the primary
          network            interface'
        type: string
      - in: query
        name: KernelId
        description: The ID of the kernel
        type: string
      - in: query
        name: KeyName
        description: The name of the key pair
        type: string
      - in: query
        name: MaxCount
        description: The maximum number of instances to launch
        type: string
      - in: query
        name: MinCount
        description: The minimum number of instances to launch
        type: string
      - in: query
        name: Monitoring
        description: The monitoring for the instance
        type: string
      - in: query
        name: NetworkInterface.N
        description: One or more network interfaces
        type: string
      - in: query
        name: Placement
        description: The placement for the instance
        type: string
      - in: query
        name: PrivateIpAddress
        description: '[EC2-VPC] The primary IPv4 address'
        type: string
      - in: query
        name: RamdiskId
        description: The ID of the RAM disk
        type: string
      - in: query
        name: SecurityGroup.N
        description: '[EC2-Classic, default VPC] One or more security group names'
        type: string
      - in: query
        name: SecurityGroupId.N
        description: One or more security group IDs
        type: string
      - in: query
        name: SubnetId
        description: '[EC2-VPC] The ID of the subnet to launch the instance into'
        type: string
      - in: query
        name: UserData
        description: The user data to make available to the instance
        type: string
      responses:
        200:
          description: OK
      tags:
      - Server Instance
  /?Action=UnmonitorInstances:
    get:
      summary: Unmonitor Instances
      description: Disables detailed monitoring for a running instance.
      operationId: unmonitorinstances
      x-api-path-slug: actionunmonitorinstances-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: InternetGatewayId
        description: The ID of the Internet gateway
        type: string
      - in: query
        name: VpcId
        description: The ID of the VPC
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