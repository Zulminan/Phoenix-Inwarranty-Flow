# Postman API Automation integration with GitHub Actions #

This repository is a demonstration for POC for integrating Postman test with GitHub Actions. The tests are written in Postman and they are executed on the Virtual Machine with the help of newman and newman-reporter-htmlextra.
GitHub Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The project runs on the scheduled time with the help of CRON job.

The HTML report is archived and kept in the artifacts section for the team to download. Along with that they can view the report directly from the GitHub page : https://zulminan.github.io/Phoenix-Inwarranty-Flow/
The latest report is mailed to the team members using gmail SMTP.

# About Me #
Hi my name is Zulminan Ahmed. I have 8 years of Experience in IT and 5 years of experience in Automation Testing. My skill set includes UI Automation with Selenium WebDriver and in API Testing I used Postman and Rest Assured and you can connect with me over LinkedIn : https://www.linkedin.com/in/zulminanahmed786/

# Testing Coverage #
1. Happy flow testing
2. Negative Testing and Edge case testing
3. Token testing
4. Data driven testing with CSV
5. Schema validation
6. Secrets management with GitHub secrets

# Tech Stack #
1. Postman
2. Nodejs v22
3. Newman
4. Newman-Reporter-Htmlextra
5. GitHub Actions
6. Gmail SMTP
7. GitHub Pages
8. CSV For Data Driven Testing
9. AWS EC2 Instance For Self Hosted GitHub Runner

# GitHub Pages #
You can directly view the latest test report of the Postman test at the GitHub page link : https://zulminan.github.io/Phoenix-Inwarranty-Flow/

# HTML Report #
The report will be created in the newman folder

![Postman Report](https://raw.githubusercontent.com/Zulminan/Phoenix-Inwarranty-Flow/static-content/newman-report.png)

# Project Structure #

```
Phoenix Inwarranty Flow 
├─ Inwarranty-flow Collection.postman_collection.json # Collection File
├─ QA.postman_environment.json # Environment File
└─ testdata.csv # Test Data File
```

# How to run the Project? #
You can run the project on your local system for that:
1. Clone the project on local system : ``` https://github.com/Zulminan/Phoenix-Inwarranty-Flow.git ```
2. Install Nodejs and NPM from : ``` https://nodejs.org/en ```
3. Install Newman using ``` npm install -g newman ```
4. Install Newman-reporter-htmlextra using ``` npm install -g newman-reporter-htmlextra ```
5. Run the Newman command :
        
          
          newman run 'Inwarranty-flow Collection.postman_collection.json' \
          -e QA.postman_environment.json \
          -d testdata.csv \
          -r cli,htmlextra \
          --reporter-htmlextra-export ./newman/index.html
          
        
