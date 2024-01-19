Here are some list and resources that I can use for source code review of different-different languages.
Currently my project is of python + django framework, and I have to perform source code review of their entire django project which includes apps, rest-api architecture, github actions, jenkins conf. database etc. 

[semgrep](https://github.com/semgrep/semgrep) - supports python language. Has both CLI and cloud platform.    
[Learning secure code review by farah hawa](https://www.youtube.com/watch?v=ajcxjnTFo6A)    
[Bandit](https://github.com/PyCQA/bandit)    
[Synk](https://app.snyk.io/)    
[Safety](https://pypi.org/project/safety/) - for finding vulnerable and outdated components stored in the local environment or requirements.txt    

### Synk
[All commands](https://docs.snyk.io/snyk-cli/commands)    
Installation on windows: `curl https://static.snyk.io/cli/latest/snyk-win.exe -o snyk.exe`    
Installation on Linux:    
```
curl https://static.snyk.io/cli/latest/snyk-linux -o snyk
chmod +x ./snyk
mv ./snyk /usr/local/bin/ 
```

2. Then we have to authorize our account using command: `snyk.exe auth`    
3. Scan for security issues:
   * `snyk monitor --all-projects --org=d768fdb7-b9cd-4e0d-8bae-70323ec6507a`

Integrate synk with the python code: [documentation](https://docs.snyk.io/integrate-with-snyk/snyk-ci-cd-integrations/github-actions-for-snyk-setup-and-checking-for-vulnerabilities/snyk-python-action)
