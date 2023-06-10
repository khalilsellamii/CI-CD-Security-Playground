# Writeup and Thoughts

For this challenge, it's pretty easy actually, just we need to install a git repository scanner to identify secrets exposed in it.

`1` Clone the duchess repository  

`2` Install a git repository scanner like gitleaks.

`3` Run gitleaks against the duchess repository to detect exposed secrets looking for the pypi token we need to submit as a flag with the command 
```
gitleaks detect -v | tee scan_results.log
cat scan_results.log | grep "pypi"
```

<p align="center">
<img src="https://github.com/khalilsellamii/CI-CD-Security-Playground/blob/main/duchess-challenge/gitleaks.png" alt="Alt text" width="700" height="350">
</p>
