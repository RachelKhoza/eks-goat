EKS-goat
This repository contains Terraform code to provision an EKS cluster on AWS. The cluster is configured to be highly available and scalable, and it is also secured with best practices in mind.

Prerequisites
To use this repository, you will need to have the following installed:

Terraform
AWS CLI
Usage
To provision an EKS cluster using this repository, follow these steps:

Clone the repository to your local machine:

Change directory to the repository:

Initialize Terraform:
"
terraform init
"

Set the Terraform variables in the variables.tf file. The following variables are required:
aws_region: The AWS region where you want to provision the EKS cluster.
eks_cluster_name: The name of the EKS cluster.
eks_node_group_size: The number of nodes in the EKS node group.
Apply the Terraform configuration:
"
terraform apply
"

Wait for the Terraform configuration to be applied. This may take several minutes.

Once the Terraform configuration has been applied, you can connect to the EKS cluster using the kubectl command-line tool:

"
kubectl get nodes
"

This should return a list of the nodes in the EKS cluster.

Secured EKS Cluster
This EKS cluster is configured with the following security best practices in mind:

The EKS cluster is provisioned in a dedicated VPC.
The EKS cluster is configured with IAM roles for service accounts 
The EKS cluster is configured with the Kubernetes Audit Logging feature.
