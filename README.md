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

## Documentation

For detailed instructions on setting up and configuring each task, please refer to the documentation available in the respective task directories.

## Contributions

Contributions to this project are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
