# Writeup and Thoughts

For this challenge, it's pretty easy actually, just we need to install a git repository scanner to identify secrets exposed in it.

`1` Clone the duchess repository  

`2` Install a git repository scanner like gitleaks.

`3` Run gitleaks to detect exposed secrets looking for the pypi token we need to submit as a flag.
