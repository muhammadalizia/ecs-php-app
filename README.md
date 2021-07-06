# Amazon ECS PHP Simple Demo App along with Deploying an App in an ECS Cluster via Pipeline
Directions on how to launch this sample app on Amazon ECS can be found in the documentation: [Docker basics](http://docs.aws.amazon.com/AmazonECS/latest/developerguide/docker-basics.html).

# Tasks:
1. Download the application source:
git clone https://github.com/awslabs/ecs-demo-php-simple-app
and test it on my PC via docker.
2. Create an ECR repo and push the code from PC to ECR.
3. Create An ECS Cluster along with Task Definition for the containers to run in the cluster.
4. Create a service based on the Task Definition to schedule and manage tasks.
5. Once the application started running successfully in the cluster, created a git repository & pushe the code for AWS CodeBuild for building docker image.
6. Create CodeBuild Project to pull the code from git and build the image and push it to ECR.
7. Create CodePipeline to use git as source, CodeBuild for build and deploy into the ECS cluster.
And finally, as soon as the code is deployed, the application will run in the container(s).
Changes on Git source will trigger pipeline to update the code and deploy the updated code in ECS.

# Important Note:
buildspec.yml is used for build specification reference for CodeBuild, gothrought the file and make the changes per requirements.
