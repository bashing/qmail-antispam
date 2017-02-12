# qmail-antispam
Qmail limit number of emails sent by user or domain per day


This script limit the number of emails sent ​​per user per day. If the user reached a maximum preset, the script will change the password and an email is sent to the administrator.

To install:

You must have qmt with spamdyke installed.
Save and execute permissions to this script as: /home/vpopmail/bin/qmail-antispam
Create this file: /etc/qmailadmin/qmail-spam/blacklist
In the crontab add
*/5 * * * * /home/vpopmail/bin/qmail-antispam >> /var/log/maillog 2>&1
Review the logs so to check if it works:

tail -f /var/log/maillog | grep "qmail-antispam"

