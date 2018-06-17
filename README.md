Yo world v1! - via nginx
=================

docker build -t nifyworx/yo-world-nginx-v1:latest .
docker run -p 80:80 nifyworx/yo-world-nginx-v1:latest

curl localhost:80 | http://localhost:80
curl localhost:80/v1/ | http://localhost:80/v1/


NOTE: Dynamic port mappings is only supported on ALB not ELB (Classic Load Balancer) - need an explicity hostPort to containerPort bindings


Task Definition: task-def-yo-world-v1:1

{
  "executionRoleArn": null,
  "containerDefinitions": [
    {
      "dnsSearchDomains": null,
      "logConfiguration": null,
      "entryPoint": null,
      "portMappings": [
        {
          "hostPort": 0,
          "protocol": "tcp",
          "containerPort": 80
        }
      ],
      "command": null,
      "linuxParameters": null,
      "cpu": 0,
      "environment": [],
      "ulimits": null,
      "dnsServers": null,
      "mountPoints": [],
      "workingDirectory": null,
      "dockerSecurityOptions": null,
      "memory": 128,
      "memoryReservation": null,
      "volumesFrom": [],
      "image": "niftyworx/yo-world-nginx-v1:latest",
      "disableNetworking": null,
      "healthCheck": null,
      "essential": true,
      "links": null,
      "hostname": null,
      "extraHosts": null,
      "user": null,
      "readonlyRootFilesystem": null,
      "dockerLabels": null,
      "privileged": null,
      "name": "container-name-yo-world-v1"
    }
  ],
  "placementConstraints": [],
  "memory": null,
  "taskRoleArn": null,
  "compatibilities": [
    "EC2"
  ],
  "taskDefinitionArn": "arn:aws:ecs:us-east-1:<addmyawsaccount#>:task-definition/task-def-yo-world-v1:1",
  "family": "task-def-yo-world-v1",
  "requiresAttributes": [],
  "requiresCompatibilities": [
    "EC2"
  ],
  "networkMode": null,
  "cpu": null,
  "revision": 1,
  "status": "ACTIVE",
  "volumes": []
}
