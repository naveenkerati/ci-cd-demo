# Continous Deployment of Docker images

This Repo is a sample demo for continous Deployment of docker image in AWS ECS. The idea is to build a docker image and push th docker to AWS ECS cluster whenever there is change in source code.

**This solution works like follows:**

* Push code to Github Repo.

* AWS Codepipeline pulls the changes in the Repository and start's processing pipeline. This is called Source stage.

* Each stage(Source, Build and Staging) in codepipeline uses the artifacts that are stored in S3 Buket.

* In Build Phase *AWS CodepBuild* will compile the code, run unit tests and integration tests,build the docker image and pushes the image to *AWS ECR* and produces artifacts that are ready to deploy.



