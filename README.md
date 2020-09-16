

# Robot Framework (Test Automation) Job Scheduler & Reporting (Web App)
#### Prototype used @ Cloud Genix Networking Team (https://www.cloudgenix.com/)
#### Developed at the Palo Alto Networks Hackathon 2020 (24 hours)

1) Set up "lib.django.robot_execute" with a function to track directory of testcases or github repository RobotService()
2) Set Up with Django and Run

GO TO http://127.0.0.1:8000/robotjobs/scheduler/

### Features
Job Scheduler: 
- Running Full, Intermediate, Sanity Test Cases
- Running custom selection of testcases
- Running Test Cases by filtering on Job List, Test Suites and Features
  - For example you can run Route Manager ClI Tests under the Routing Feature List, you can run VPN tests cases (many more), or you can mix and match various test       cases from different feature list to create a custom job
- All testcases run as background processes using Celery and Redis to pass messages between a Django and Celery workers
- The RobotService() is not in this code, but is the underlying service that runs testcases and reports various statuses for all jobs

Job Results View (Can only be viewed, if you have your own RobotService running):
- Shows the progress of the jobs running (YET TO START, ERROR, RUNNING) 
- Shows progress of each test case, if you want to dive deeper (PASS, FAIL,  RUNNING)

Completed Jobs (Can only be viewed, if you have your own RobotService running): 
- Some thing as Job Results View, but only for Completed Jobs


