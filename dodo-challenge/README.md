# Challenge Description

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/dodo-challenge/description.png" alt="Alt text" width="500" height="300">
</p>

# Write-up and Thoughts

After accessing the Gitea hosted locally on port 3000 with the credentials  
```
username : thealice
password : thealice
```
We need to follow these steps :  

`1` Clone the dodo repository  

`2` Modify the main.tf file to set up the access control list ACL to publically readable instead of privare .  

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/dodo-challenge/main_tf_file.png" alt="Alt text" width="800" height="350">
</p>

`3` Add a new checkov.yaml file with this content:

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/dodo-challenge/checkov.yaml.png" alt="Alt text" width="800" height="350">
</p>

> the soft_fail keyword is used to enable soft-fail mode, allowing Checkov to continue scanning and reporting issues even if a check encounters an error.

`4` Commit and push the changes to the original repository

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/dodo-challenge/git.png" alt="Alt text" width="800" height="350">
</p>

`5` Check out the console output of the Jenkins Server to retrieve the flag after the success of the pipeline's build

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/dodo-challenge/jenkins_build.png" alt="Alt text" width="800" height="350">
</p>
<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/dodo-challenge/flag.png" alt="Alt text" width="800" height="350">
</p>
