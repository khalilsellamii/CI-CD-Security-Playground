# CI-CD-Security-Playground

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/images/cicdgoatbycider.png" alt="Alt text" width="1000" height="200">
</p>  
  


This is a deliberately vulnerable CI/CD environment provided by cider-securiy-research in order to learn and practice CI/CD security through a set of different challenges, enacted against a real, full blown CI/CD environment. The challenges cover the Top 10 CI/CD Security Risks, including Insufficient Flow Control Mechanisms, PPE (Poisoned Pipeline Execution), Dependency Chain Abuse, PBAC (Pipeline-Based Access Controls) ...  

## Components
The project’s environment is based on Docker containers and can be run locally. These containers are:

1.Gitea (minimal git server)  
2.Jenkins  
3.Jenkins agent  
4.LocalStack (cloud service emulator that runs in a single container)  
5.Prod - contains Docker in Docker and Lighttpd service  
4.CTFd (Capture The Flag framework)  
7.GitLab  
8.GitLab runner  
9.Docker in Docker  

## Architecture  
The different images are configured to interconnect in a way that creates fully functional pipelines.  
<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/images/Architecture_generale.png" alt="Alt text" width="1000" height="500">
</p>  

## Basic Notions

### What is Jenkins ? 
Jenkins is an open-source automation server that helps automate various aspects of software development, including building, testing, and deploying applications. It provides a platform for Continuous Integration (CI) and Continuous Delivery (CD) practices, allowing development teams to automate their software delivery pipeline.  

### What is Gitlab ? 
GitLab is a web-based DevOps platform that provides a complete set of tools and features for managing the entire software development lifecycle. It offers a Git repository management system along with integrated continuous integration, continuous delivery, and deployment capabilities.  

### What is Gitea ?
Gitea is an open-source self-hosted Git service and web-based Git repository management system. It provides a lightweight and easy-to-use interface for managing Git repositories, issue tracking, code reviews, and collaboration. Gitea is designed to be simple, fast, and highly customizable, making it a popular choice for individuals, small teams, and organizations looking for a self-hosted Git solution.  
