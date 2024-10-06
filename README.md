This repository contains scripts and Kubernetes manifests for deploying the Nodejs application with Postgres Database on an AWS EKS cluster with an accompanying ECR repository and EBS volumes. The deployment includes setting up an Ingress controller, monitoring with Prometheus and Grafana, and a continuous deployment pipeline.

Prerequisites
__________________________________________________________________________________________________________________________________________________________________________________________________________________
. AWS CLI configured with appropriate permissions	                                                                                                                                                                     
. Docker installed and configured	                                                                                                                                                                                     
. kubectl installed and configured to interact with your Kubernetes cluster	                                                                                                                                           
. Terraform installed                                                                                                                                                                                                 	                                                                                                                                                                                                                    
. Helm installed                                                                                                                                                                                                      	                                                                                                                                                                                                                   
. GitHub_CLI installed	                                                                                                                                                                                                                                                                                                                                                                                                                    
. Beekeeper-Studio For Database Access                                                                                                                               
___________________________________________________________________________________________________________________________________________________________________
chmod +x build.sh                                                                                                                                                                                                                                                                                                                         
./build.sh             #run for the script that contains some variables that you need to customize according to your AWS environment and deployment requirements.

./github_secrets.sh    #Use the GitHub CLI to add your AWS credentials (secret key & secret access key) to GitHub Secrets, but ensure you have the GitHub CLI (gh) installed and authenticated.

cat ~/.kube/config | base64  # to access kubernetes cluster, add kubconfig ti githubsecrets. Copy the encoded output to your clipboard, Paste the base64-encoded KUBECONFIG data into the secret's value field in github repository.

