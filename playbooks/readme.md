# Ansible Playbooks

This directory contains Ansible playbooks used in the DevOps Real-Time Project 1. These playbooks automate various tasks related to deployment, configuration, and management of infrastructure and applications. Each playbook focuses on a specific aspect of the project's workflow. 

## Playbook List

### 1. create_directory.yml

This playbook is responsible for creating a directory and copying the generated JAR file and Dockerfile to the designated directory. It performs the following tasks:

- Creates a directory for storing the artifacts.
- Copies the generated JAR file to the directory.
- Copies the Dockerfile to the directory.

Usage:

```shell
ansible-playbook playbooks/create_directory.yml
```

Make sure to modify the playbook variables and paths to match your project requirements.

### 2. push_dockerhub.yml

This playbook is used to push the Docker image to DockerHub for storage and distribution. It requires the following variables:

- `JOB_NAME`: The name of the Jenkins job.
- `BUILD_ID`: The ID of the Jenkins build.
- `dockerhub_user`: DockerHub username.
- `dockerhub_pass`: DockerHub password.

Usage:

```shell
ansible-playbook playbooks/push_dockerhub.yml \
    --extra-vars "JOB_NAME=<job_name>" \
    --extra-vars "BUILD_ID=<build_id>" \
    --extra-vars "dockerhub_user=<dockerhub_username>" \
    --extra-vars "dockerhub_pass=<dockerhub_password>"
```

Replace `<job_name>`, `<build_id>`, `<dockerhub_username>`, and `<dockerhub_password>` with the appropriate values.

### 3. create_pod_on_eks.yml

This playbook deploys the application on Amazon Elastic Kubernetes Service (EKS). It requires the following extra variable:

- `JOB_NAME`: The name of the Jenkins job.

Usage:

```shell
ansible-playbook playbooks/create_pod_on_eks.yml \
    --extra-vars "JOB_NAME=<job_name>"
```

Replace `<job_name>` with the desired value.

Please note that proper setup and configuration of Ansible inventory, credentials, and variables are necessary for the successful execution of these playbooks.

