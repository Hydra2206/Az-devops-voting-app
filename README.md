# Az-devops-voting-app
Deploying a multi microservices voting application using Azure Devops

Implementation steps:
1) using a docker sample repo for this project
2) Migrated that repo into Azure devops repos
3) Created 3 pipelines for 3 microservices - result, worker, vote
4) created a self-hosted runner & configure it to run these pipelines
5) created a container registry so that we can build & push images
6) created a aks, installing argocd & configuring
