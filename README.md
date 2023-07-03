# DevOps Real-Time Project 1

[![Build Status](https://img.shields.io/github/workflow/status/imranark/devops_real_time_project_1/Build%20and%20Test)](https://github.com/imranark/devops_real_time_project_1/actions)

This repository contains a real-time DevOps project that demonstrates the automation of software development and deployment processes using Jenkins. The project consists of various tasks that streamline workflows and enhance productivity.

## Project Overview

The project focuses on building, testing, analyzing code, generating artifacts, deploying, and sending notifications. It includes the following tasks:

- **Clean Workspace**: Cleans the workspace before starting the build process.
- **Code Checkout**: Checks out the source code from a Git repository.
- **Modified Image Tag**: Modifies the image tag in relevant files for unique identifiers.
- **Build**: Builds the application using Maven.
- **Sonar Scanner**: Performs static code analysis using SonarQube.
- **Copy JAR & Dockerfile**: Copies generated artifacts to a designated directory.
- **Push Image on DockerHub**: Pushes Docker image to DockerHub for storage and distribution.
- **Deployment on EKS**: Deploys the application on Amazon Elastic Kubernetes Service (EKS).

## Getting Started

To use this project, follow these steps:

1. Clone the repository using the following command:
    ```
    git clone https://github.com/imranark/devops_real_time_project_1.git
    ```

2. Configure your Jenkins instance with the necessary plugins and credentials.

3. Set up a Jenkins pipeline with the `Jenkinsfile` provided in this repository.

4. Customize the pipeline stages, environment variables, and additional configurations based on your project requirements.

5. Run the pipeline and monitor the build and deployment processes.

## Task 1: Clean Workspace

This task is responsible for cleaning the workspace before starting the build process. It ensures a clean environment for the subsequent stages. It involves the following step:

- Clean the workspace using the `cleanWs()` function.

## Task 2: Code Checkout

This task checks out the source code from a Git repository. It fetches the latest code changes and prepares it for the build process. It involves the following step:

- Clone the source code repository using the `git` command.

## Task 3: Modified Image Tag

This task modifies the image tag in the relevant files to ensure a unique identifier for each build. It involves the following steps:

- Use the `sed` command to replace the image tag in the `dep_svc.yml` playbook.
- Update the image tag in the `index.jsp` file.

## Task 4: Build

This task builds the application from the source code. It involves the following step:

- Use Maven to clean, install, and package the application using the `mvn` command.

## Task 5: Sonar Scanner

This task performs static code analysis using SonarQube. It involves the following steps:

- Configure the SonarQube token using the `sonar_token` environment variable.
- Run the SonarQube scanner using Maven and pass the necessary parameters such as project name, project key, SonarQube host URL, and token.

## Task 6: Copy JAR & Dockerfile

This task copies the generated JAR file and Dockerfile to a designated directory. It involves the following step:

- Use Ansible to execute the `create_directory.yml` playbook.

## Task 7: Push Image on DockerHub

This task pushes the Docker image to DockerHub for storage and distribution. It involves the following steps:

- Configure the DockerHub credentials using the `dockerhub_user` and `dockerhub_pass` environment variables.
- Use Ansible to execute the

 `push_dockerhub.yml` playbook, passing the necessary variables such as job name, build ID, DockerHub username, and password.

## Task 8: Deployment on EKS

This task deploys the application on Amazon Elastic Kubernetes Service (EKS). It involves the following steps:

- Use Ansible to execute the `create_pod_on_eks.yml` playbook, passing the job name as an extra variable.

## Documentation

For detailed instructions on setting up and configuring each task, please refer to the documentation available in the respective task directories.

## Contributions

Contributions to this project are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
