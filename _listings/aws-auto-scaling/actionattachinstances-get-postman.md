{
  "info": {
    "name": "AWS Auto Scaling API Attach Instances",
    "_postman_id": "acd23b43-5e8f-4fc0-858a-751925c739f4",
    "description": "Attaches one or more EC2 instances to the specified Auto Scaling group.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Server Instance",
      "item": [
        {
          "id": "5328b249-e1d6-48bc-8aa8-d8f7c309c841",
          "name": "attachInstances",
          "request": {
            "url": "http://example.com/api/?Action=AttachInstances?AutoScalingGroupName=AutoScalingGroupName&InstanceIds.member.N=InstanceIds.member.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Attaches one or more EC2 instances to the specified Auto Scaling group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "04519b7f-dc00-462e-965b-fa273ca38752"
            }
          ]
        }
      ]
    }
  ]
}