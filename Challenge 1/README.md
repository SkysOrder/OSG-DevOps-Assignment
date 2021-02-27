## Challenge 1
To maintain High Availablity, it is best to adopt Amazon Elastic Kubernetes Service (Amazon EKS) from AWS.

Kuberenetes is a orchestration tool that provides many functions which one of them is "Self healing". With Self Healing, containers are restarted when they fail, replaces containers and kills containers when they don't respond to health checks. 

With EKS, we are able to provision Kubernetes clutsters to hosts our service and nodes (Master and Slave). Using the benefits of Kubernetes, EKS is aable to automatically detects and replaces unhealthy control plane nodes, provides on-demand, zero downtime upgrades and patching. This will result in little to no downtimes. This is a highly available which the company requires.

The company currently have inconsitent traffic which resuls in increased costs. This issue can be tackled with AWS Fargate. AWS Fargate is serverless compute engine for containers. It allocates the right amount of compute, eliminating the need to choose instances and scale cluster capacity. This reduces costs as there will no over provisioning and paying for the extra servers.

A classic load balancer is also recommended despite being older. This have the ability to enable both Layer 4 and 7 checks while load balancing. Moving to classic ECS would also not be a problem as Classoc Load Balancer runs on it too unlike other ELB options such as Application Load Balancer. 

AWS also provides databases which are highly available. As a B2C company, having a database with is highly available is crucial for them. Furthermore, the company would like to reduce the administrative burden of managing their SQL database. With these 2 requirements in concern, I recommend Amazon DynameDB. This database have availabilty and fault tolerance built in and is able to handle millions of requests per second. Being severless, The company would have more time doing other important tasks and notworry about the servers.

AWS Technology used
- Amazon EKS
- AWS Fargate
- Classic Load Balancer (ELK)
- DynamoDB
