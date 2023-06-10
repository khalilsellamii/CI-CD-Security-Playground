# Challenge Description

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/caterpillar-challenge/description.png" alt="Alt text" width="500" height="300">
</p>

# Writeup and Thoughts

We are performing a PPE attack on the caterpillar pipeline.

`1` We fork the repository and modify the JenkinsFile to get the gitea token, this token will grant us the permissions that we need later

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/caterpillar-challenge/jenkinsfile.png" alt="Alt text" width="800" height="350">
</p>

`2` After modifying the JenkinsFile, we create a pulll request and access to Jenkins server to chech the output console for the token which is an environment variable: 

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/caterpillar-challenge/jenkins.png" alt="Alt text" width="800" height="350">
</p>

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/caterpillar-challenge/gitoken.png" alt="Alt text" width="800" height="350">
</p>

`3` Now, we clone the repository from the gitea server with the token we grabbed from the executed pipeline

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/caterpillar-challenge/git_clone_with_token.png" alt="Alt text" width="800" height="350">
</p>

`4` We modify the JenkinsFile again, but now to retrieve the flag 
<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/caterpillar-challenge/modify_jenkinsfile.png" alt="Alt text" width="800" height="350">
</p>

`5` We get our flag encoded, we decode it and we submit

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/caterpillar-challenge/flag.png" alt="Alt text" width="800" height="350">
</p>


