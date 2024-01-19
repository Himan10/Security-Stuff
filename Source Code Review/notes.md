Better create a virtual environment before installing the tools so that you don't mess up your local environment. 

### Bandit
Command: `pip install bandit`    
Scan python code: `bandit -r directory`    
Send the output to a file: `bandit -o output_file.json`    
Exclude some directories and files: `bandit -x dir1,dir2,filename1`    

Full command: `bandit -r directory -f json -o report.json -x dir1,dir2,filename1`    
`-f` is used for specify the format.     

### Safety
Command: `pip install safety`    

Scan requirements.txt file    
1. `safety check -r requirements.txt`    
2. `cat requirements.txt | safety check --stdin`    
Save output in a file: `safety check -r requirements.txt --output json`   
***Note: packages should be mentioned with their respective versions in the requirements.txt file or else it'll generate the warning, and those packages wouldn't be checked***
