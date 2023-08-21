# Elastic Beanstalk Cheatsheet
Documenting my Usage of AWS Beanstalk

## Allow Tail Logs - Configuration (Amazon Linux 2)

1. Create a file within the .ebextensions folder -

The file will contain the code below:

files:
  "/opt/elasticbeanstalk/tasks/taillogs.d/applogs.conf" :
    mode: "000755"
    owner: root
    group: root
    content: |
      /var/app/current/logging/*.log

`/var/app/current/logging/*.log` will be your logging folder.
