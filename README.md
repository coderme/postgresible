# Postgresible
An Ansible playbook to automate installation/upgrade/configuration of postgresql. 

## Features
* Teak some sysctl.conf value for performance.
* Add cronjob to perform daily backup for all databases.
* Support Debian OS for now.

## Customization
The following variables are supported:
* *backup\_dir*: control where to store the database backup files (default: '/data/backups')
* *backup\_maxage*: max age in days of database backups before we start deleting old ones (default to '7')
* *cron\_run\_hour*: at which hour cron should run (default 21)
* *cron\_run\_minute*: at which hour cron should run (default also 21)


## Usage
* Clone this repository, edit hosts
* For fresh install run: *ansible-playbook -i hosts pg\_play.yaml*
* To upgrade postgresql run: *ansible-playbook -i hosts pg\_upgrade.yaml*

