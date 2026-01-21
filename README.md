Motive of this project is to learn Azure Devops
# Az-devops-voting-app
Deploying a multi microservices voting application using Azure Devops

Implementation steps:
1) using a docker sample repo for this project
2) Migrated that repo into Azure devops repos
3) Created 3 pipelines for 3 microservices - result, worker, vote
4) created a self-hosted runner & configure it to run these pipelines
5) created a container registry so that we can build & push images
6) created a aks, installed argocd & configure it
7) creating a personal access token for repo to load into argocd, bcoz our repo is private
8) creating a script that will automatically update deployment.yaml for all 3 microservices with the new image, every time when pipeline triggers


challenges - whenever userscript is running in pipeline, after executing every line there is /r is added to the command bcoz of that command gets wrong & it won't get executed.
            problem - windows CLRF type it is adding (/r/n) after every line of script
            solution - copy my code to vs & in bottom right i can change type from CLRF -> LF & use that script only

challanges - ImagePullError - cluster is not able to pull images from container registry maybe bcoz it's a pvt registry, so you need to create a secret & pass that secret name in the deployment.yaml file
            ek aur issue that jiske karan ImagePullError aa sakta joh mere sath hua, image name incorrect that deployment.yaml me, jiske karan image pull nahi kar para tha


