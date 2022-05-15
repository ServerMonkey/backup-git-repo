# backup-git-repo
Backup multible Git repositories by cloning them.

Tested on Debian 11

### Example installation
Add these lines:  
`:syslogtag, startswith, "backup-git-repo" /var/log/backup-custom.log`  
`& stop`  
to:  
`/etc/rsyslog.d/00-crontab.conf`  
and run:  
`systemctl restart rsyslog.service`

Then add this to crontab:  
`0 1 * * * cronic backup-git-repo <GIT_SERVER> <BACKUP_PATH>`

### How to use
`backup-git-repo -h`
