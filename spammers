#!/bin/bash
##Script To Monitor Spammers Path
## Author Qasim
## Written Feb 21 2014 2:15 AM
## Modified on Feb 23 6:30 PM
## What It Will Do ?
## The Script Will Email You The Exact Path For Spammer

script=`awk '{ if ($0 ~ "cwd" && $0 ~ "home") {print $3} }' /var/log/exim_mainlog | sort | uniq -c | sort -nk 1 | tail -n 1 | awk '{print $1}'`

##Please Adjust The Value I Made The Default Value 1000
if [ $script -gt 1000 ]
then
awk '{ if ($0 ~ "cwd" && $0 ~ "home") {print $3} }' /var/log/exim_mainlog | sort | uniq -c | sort -nk 1 | tail -n 5 | mail -s " Script Spamming ( High Alert ) "  email-address@domain.com

fi
## END
