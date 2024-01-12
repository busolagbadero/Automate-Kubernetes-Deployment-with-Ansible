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

## ANSIBLE-PLAYBOOK
Head to the Ansible server to create a playbook for Kubernetes. Initiate the process by using an Ansible playbook to create a namespace named "my-app."

The Ansible playbook targets the local machine, utilizing the k8s module to ensure the presence of a Kubernetes namespace named "my-app" on the cluster.

![k85](https://github.com/busolagbadero/Automate-Kubernetes-Deployment-with-Ansible/assets/94229949/0827a1ad-ae85-4b3f-bd78-996713c587ef)


Modify the 'ansible.cfg' file to include a default host, eliminating the need to explicitly specify it in the command when executing the Ansible playbook.

![k86](https://github.com/busolagbadero/Automate-Kubernetes-Deployment-with-Ansible/assets/94229949/59dcfd73-fb42-4420-8f0c-1014e40e70af)

![k813](https://github.com/busolagbadero/Automate-Kubernetes-Deployment-with-Ansible/assets/94229949/b3a3544f-4f7e-430b-977c-1c4bfc760ec9)

![k87](https://github.com/busolagbadero/Automate-Kubernetes-Deployment-with-Ansible/assets/94229949/641d8a6a-1c7f-4fc6-8b28-6f16f18521c5)

## DEPLOY NGINX APP

![k88](https://github.com/busolagbadero/Automate-Kubernetes-Deployment-with-Ansible/assets/94229949/c6f5369e-0794-4266-8dca-c629d0ede975)

The provided Ansible playbook snippet titled "Deploy NGINX app" uses the k8s module to facilitate the deployment of an NGINX application on an Amazon EKS cluster. The playbook specifies the source file for the Kubernetes resource definition (/home/ubuntu/nginx.yaml), sets the desired state to "present" to ensure the NGINX app is deployed, and designates the target namespace as "my-app."

![k89](https://github.com/busolagbadero/Automate-Kubernetes-Deployment-with-Ansible/assets/94229949/84197d0a-7317-4f3d-949c-ed5177c5f559)

![k810](https://github.com/busolagbadero/Automate-Kubernetes-Deployment-with-Ansible/assets/94229949/ae6473ac-213f-408f-9b38-8a27245accd1)

![k811](https://github.com/busolagbadero/Automate-Kubernetes-Deployment-with-Ansible/assets/94229949/b4e10581-ee9e-48a5-90c3-bcd797184cd8)

To eliminate the need for repetitive specification of the kubeconfig file in each task of the playbook, I exported the file location using the command `export K8S_AUTH_KUBECONFIG=the_location_of_ .kube/config`. Subsequently, I reran the playbook to confirm its successful execution.

![k812](https://github.com/busolagbadero/Automate-Kubernetes-Deployment-with-Ansible/assets/94229949/d1d55f7a-a12e-42d0-be51-449bd0af483c)








