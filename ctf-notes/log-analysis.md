# Log Analysis

-Search For IPs or specifics in log file

 -cut & awk commands: --Get unique IP and Count them:

`cat access.log | awk '{print $1}' | sort | uniq -c | sort -nr`

 `cat access.log | cut -d " " -f 1 | sort | uniq -c | wc -l`

 `cat access.log | awk '{print NR,$6}'`

 `cat access.log | awk '{ if($9 == "400") print NR,$9;}'`

CAINE use tool - log2timeline

#### Remove White Space

$ man tr  


In order to wipe all whitespace including newlines you can try:

```text
cat file.txt | tr -d " \t\n\r" 
```

You can also use the character classes defined by tr \(credits to [htompkins](https://stackoverflow.com/users/315868/htompkins) comment\):

```text
cat file.txt | tr -d "[:space:]"
```

For example, in order to wipe just horizontal white space:

```text
cat file.txt | tr -d "[:blank:]"
```

