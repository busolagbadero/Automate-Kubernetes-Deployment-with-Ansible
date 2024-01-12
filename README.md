# Automate Kubernetes Deployment with Ansible

## OVERVIEW
This repository provides a set of automation scripts to streamline the process of deploying a Kubernetes cluster on Amazon EKS using Terraform and configuring it with Ansible. The end goal is to deploy an NGINX application on the Kubernetes cluster, showcasing a basic deployment and service setup.

# KUBERNETES CLUSTER
Created a Terraform script to provision the Amazon EKS cluster, I initiated the Terraform setup and executed `terraform apply`. Following the successful completion of this step, the EKS cluster was launched. I navigated to the Ansible server to configure Kubernetes and manage the newly created cluster.

![k81](https://github.com/busolagbadero/Automate-Kubernetes-Deployment-with-Ansible/assets/94229949/73c67c1d-3ba5-4837-9e76-f4cdb0d8fb92)

![k82](https://github.com/busolagbadero/Automate-Kubernetes-Deployment-with-Ansible/assets/94229949/b90b4988-e85d-4034-ab3c-e8275b531afc)

## KUBERNETES.CORE.K8S MODULE
The kubernetes.core.k8s module in Ansible is essential for effectively managing Kubernetes (K8s) objects within your infrastructure.
Before employing the kubernetes.core.k8s module for Kubernetes object management in Ansible, it is crucial to have the following requirements installed on the host that executes this module:

Python Version: Ensure that Python is installed with a version equal to or higher than 3.6.
Kubernetes Module: Install the Kubernetes module with a version of 12.0.0 or later.
PyYAML Library: Ensure that the PyYAML library is installed with a version of 3.11 or later.
jsonpatch Library: Install the jsonpatch library to support the required functionalities.

![k83](https://github.com/busolagbadero/Automate-Kubernetes-Deployment-with-Ansible/assets/94229949/01067cc7-3d46-4542-a274-5ce8604001b7)

![k84](https://github.com/busolagbadero/Automate-Kubernetes-Deployment-with-Ansible/assets/94229949/a0007fb7-b96b-4b91-8715-4def35bb6ba0)



