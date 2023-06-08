# Challenge Description

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/mad-hatter-challenge/challenge_description.png" alt="Alt text" width="500" height="500">
</p>

# Write-up and thoughts

After accessing the Gitea hosted locally on port 3000 with the credentials  
```
username : thealice
password : thealice
```
We need to follow these steps :

`1`  Modify the Makefile file in the main branch under the Wonderland/mad-hatter repository to retrieve the flag by adding the following command :
```
echo "${FLAG}" | base32
```
<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/mad-hatter-challenge/modify_makeFile.png" alt="Alt text" width="800" height="350">
</p>

`2` Commit and push the changes made on the main branch.  

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/mad-hatter-challenge/git.png" alt="Alt text" width="800" height="350">
</p>

`3` Check the Jenkins server hosted on localhost:8080
<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/mad-hatter-challenge/jenkins_changes.png" alt="Alt text" width="800" height="350">
</p>

`4` Check the pipeline build results in the output console to retrieve the flag 
<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/mad-hatter-challenge/Jenkins_Build.png" alt="Alt text" width="800" height="350">
</p>

`5` Decode the flag and submit it 
<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/mad-hatter-challenge/flag.png" alt="Alt text" width="800" height="350">
</p>




