For CICD, I would be using AWS CodePipeline.

I will create 3 different branches in the repository of the appplications. I can name them as DEV, UAT and Production to match the environments.

In CodePipeline, I will also create 3 different pipelines for the environments. In each pipeline, I'll add in the stages of Checkout, Build and Deploy.

In Checkout stage, I would link it to the application on Github and use the branch that I want to use for the pipeline. For the DEV pipeline, I'll use the DEV branch.
In this stage, it defines the branch and environment it will be using. It willl also detect changes in Github when changes and made. Once a change is detected, it will be triggered to run the pipeline.

In Build stage, I can turn the application into a docker image and store in the AWS Elastic Container Repository. I can also attached unit testing and monitoring tools before moving on to deploy. This can all be done with a buildspec file that can be customised.

In the Deploy stage, this the part where load balancer, subnets and security groups be added in. The load balancer would have the domain where the application be accessed by the ips allowed in the security group.


I mentioned the different pipelines as I assume that the Developers would need a server to test any new features that the compnay plans to add. The UAT team would also need a server to make sure everything in working as intended before finally moving on to production.

The whole process would be automatic and thus, it fufills DevOps goal of CICD.
