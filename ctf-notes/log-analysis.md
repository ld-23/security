# Log Analysis

-Search For IPs or specifics in log file

 -cut & awk commands: --Get unique IP and Count them:

`cat access.log | awk '{print $1}' | sort | uniq -c | sort -nr`

 `cat access.log | cut -d " " -f 1 | sort | uniq -c | wc -l`

 `cat access.log | awk '{print NR,$6}'`

 `cat access.log | awk '{ if($9 == "400") print NR,$9;}'`

