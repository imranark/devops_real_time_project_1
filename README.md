Jenkins Tasks
This repository contains a collection of Jenkins tasks that can be used to automate various aspects of your software development and deployment processes. Each task is designed to streamline your workflows and enhance your productivity.

Task 1: Clean Workspace
This task is responsible for cleaning the workspace before starting the build process. It ensures a clean environment for the subsequent stages. It involves the following step:

Clean the workspace using the cleanWs() function.
Task 2: Code Checkout
This task checks out the source code from a Git repository. It fetches the latest code changes and prepares it for the build process. It involves the following step:

Clone the source code repository using the git command.
Task 3: Modified Image Tag
This task modifies the image tag in the relevant files to ensure a unique identifier for each build. It involves the following steps:

Use the sed command to replace the image tag in the dep_svc.yml playbook.
Update the image tag in the index.jsp file.
Task 4: Build
This task builds the application from the source code. It involves the following step:

Use Maven to clean, install, and package the application using the mvn command.
Task 5: Sonar Scanner
This task performs static code analysis using SonarQube. It involves the following steps:

Configure the SonarQube token using the sonar_token environment variable.
Run the SonarQube scanner using Maven and pass the necessary parameters such as project name, project key, SonarQube host URL, and token.
Task 6: Copy JAR & Dockerfile
This task copies the generated JAR file and Dockerfile to a designated directory. It involves the following step:

Use Ansible to execute the create_directory.yml playbook.
Task 7: Push Image on DockerHub
This task pushes the Docker image to DockerHub for storage and distribution. It involves the following steps:

Configure the DockerHub credentials using the dockerhub_user and dockerhub_pass environment variables.
Use Ansible to execute the push_dockerhub.yml playbook, passing the necessary variables such as job name, build ID, DockerHub username, and password.
Task 8: Deployment on EKS
This task deploys the application on Amazon Elastic Kubernetes Service (EKS). It involves the following steps:

Use Ansible to execute the create_pod_on_eks.yml playbook, passing the job name as an extra variable.
Please refer to the respective playbook files in the repository for more detailed instructions on setting up each task.
