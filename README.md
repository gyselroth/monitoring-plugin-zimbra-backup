# Monitoring Plugin: Galera cluster

### Description
Check if a zimbra backup is available and successfully executed since a specific time.

### Usage
    -h Shows this message
    -w [Default: 43200] Warning in seconds (difference between now and the last possible time to throw a warning)
    -c [Default: 86400] Critical in seconds (difference between now and the last possible time to throw a critical)

### Example
./check_zimbra_backup -w 86400 -c10000
last zimbra backup full-20170410.230200.505 is OK

### Install 
* Copy check_zimbra_backup to (all) your zimbra mail store server
* This check is required to run on the zimbra host itself therefore you need to remotely excute this check via nrpe, ssh or something similar.
* create a service/exec in your monitoring engine to execute the remote check
