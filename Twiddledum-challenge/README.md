# Challenge Description

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/Twiddledum-challenge/description.png" alt="Alt text" width="700" height="500">
</p>

# Write-up and thoughts

After accessing the Gitea hosted locally on port 3000 with the credentials  
```
username : thealice
password : thealice
```
We need to follow these steps :  

`1` Clone the repository and modify the index.js file:

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/Twiddledum-challenge/index_js.png" alt="Alt text" width="800" height="350">
</p>

`2` Add a new tag and push the changes
<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/Twiddledum-challenge/git_tags_%26_push.png" alt="Alt text" width="800" height="350">
</p>

`3` Check the gitea for the added tag 
<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/Twiddledum-challenge/new_tag.png" alt="Alt text" width="800" height="350">
</p>

`4` Now on the Jenkins server, manually trigger the twiddledum pipeline to execute the new pipeline Jobs:

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/Twiddledum-challenge/jenkins_manual_build.png" alt="Alt text" width="800" height="350">
</p>

`5` Check the console output for the executed job to get the flag 
<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/Twiddledum-challenge/flag.png" alt="Alt text" width="800" height="350">
</p>
