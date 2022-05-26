# import-cluster-on-rhacm
A simple playbook to automate the cluster import on RHACM using AWS Secret Manager.

## Requirements 

- Python >= 3.6 

- Python botocore, boto3, kubernetes

- kubernetes.core collection

- Ansible Version >= 2.9 

## AWS Secret Manager Secrets 

The secrets imported from AWS Secret Manager have the following format: 

{"api":"https://api.clustername.basedomain:6443","token":"sha256~xxxxxxxxxxxxxx"}

## Usage 

ansible-playbook import-on-rhacm.yaml  --extra-vars "managed_cluster_name=<managed_cluster_name> aws_access_key='<aws_access_key>' aws_secret_key='<aws_secret_key>' cluster_type=<cluster_type>"
