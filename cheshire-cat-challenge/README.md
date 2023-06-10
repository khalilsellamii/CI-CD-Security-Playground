# Challenge Description

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/cheshire-cat-challenge/description.png" alt="Alt text" width="700" height="450">
</p>

# Writeup and thoughts

`1` Clone the cheshire-cat repository and create a new branch to work on .  

`2` Modify the JenkinsFile to perform a PPE (Poisoned Pipeline Execution), making the jenkins displaying our flag after executing the poisoned pipeline

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/cheshire-cat-challenge/jenkinsFile_poisoning.png" alt="Alt text" width="700" height="350">
</p>

`3` Create a pull request into the original main branch

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/cheshire-cat-challenge/gitea_pull_request.png" alt="Alt text" width="700" height="350">
</p>

`4` Access the jenkins server to build and monitor the execution of the poisoned pipeline.

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/cheshire-cat-challenge/jenkins_sucess_build.png" alt="Alt text" width="700" height="350">
</p>

`5` Check the logs of the successful build for the flag

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/cheshire-cat-challenge/flag.png" alt="Alt text" width="800" height="350">
</p>
