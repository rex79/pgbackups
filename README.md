# pgbackups
Postgresql backup script with rotated backups and optional S3 aws sync

This script let you backup all your postgresql database and save them on your AWS S3 bucket.
All you need is a working aws-cli installation and an active bucket and setup the variables on the pg_backup.config.

### Configuration
The config file is well documented, keep an eye on the rotated backups sections where you can setup how many days of daily/weekly backups you wanto to keep.

```sh
# Which day to take the weekly backup from (1-7 = Monday-Sunday)
DAY_OF_WEEK_TO_KEEP=5
# Number of days to keep daily backups
DAYS_TO_KEEP=7
# How many weeks to keep weekly backups
WEEKS_TO_KEEP=5
```

For the aws configuration the only things you need to setup is the bucket name
```sh
AWS_BUCKET=foo
```
You can see how to setup a full working aws-cli here: http://docs.aws.amazon.com/cli/latest/userguide/installing.html
