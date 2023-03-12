|   |   |
|---|---|
|Date| 2023/03/12|
|Tags| #Cron |

# HowTo prevent duplicate Cron-jobs running with flock?

The scenario is a quite long running job, that should be looking in short intervals if it could be started.
My use case is the upload of data as quick as it is available. The upload will last some hours. In this time the job should not be started a second or even more time. Cause this would cause trouble.

Job runtime ~ 4h
Interval to start the job < 1h

While googling this I found a lot solutions using some small scripts.  
Better an easier solution is to use [flock](https://manpages.debian.org/jessie/manpages-de/flock.1.de.html).

Example of a cronjob running each minute, but never twice.

`* * * * * /usr/bin/flock -n /tmp/my_cron_job.lockfile /usr/local/bin/my_cron_job`

# [Startpage](/)
