# Schedule - Github Action use crontab-generator to trigger a workflow at specified timing

## Objective
- To trigger workflow one time at specified timing
---
# Steps:

## 1. Github
- Create a new repository (remember to Add a README file)✅
- Go to Actions and create workflow (main.yml) 

## 2. Visuol Studio Code (VSC)
- Update files (e.g Dockerfile, main.yml, etc) and save the changes
- Push to Github (```  git add .  ```      /      ```  git commit -m "Remark"  ```      / ``` git push ``` )
- After push, go to Github to check the workflow is running successfully

### Update main.yml 
```
name: Master
on:
  push:
    branches:
      - master
  schedule:
    - cron: '30 16 * * * '
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v1
    - name: Running
      run:
        echo "Running"
```

### Set timing to trigger workflow  
- Go to https://crontab-generator.org/
- Select the timing
- Crontab will generate the POSIX cron syntax
![image](https://user-images.githubusercontent.com/81748800/124390437-37366080-dd1e-11eb-83c4-5fce4cd85912.png)




![image](https://user-images.githubusercontent.com/81748800/124390246-38b35900-dd1d-11eb-85f3-3342e3ed0b2d.png)
