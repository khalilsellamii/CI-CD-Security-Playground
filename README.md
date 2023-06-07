# CI-CD-Security-Playground

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/images/cicdgoatbycider.png" alt="Alt text" width="1000" height="200">
</p>  
  

This is a deliberately vulnerable CI/CD environment provided by cider-securiy-research in order to learn and practice CI/CD security through a set of different challenges, enacted against a real, full blown CI/CD environment. The challenges cover the Top 10 CI/CD Security Risks, including Insufficient Flow Control Mechanisms, PPE (Poisoned Pipeline Execution), Dependency Chain Abuse, PBAC (Pipeline-Based Access Controls) ...  

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
The images are configured to interconnect in a way that creates fully functional pipelines.  
<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/images/Architecture_generale.png" alt="Alt text" width="1000" height="500">
</p>  
