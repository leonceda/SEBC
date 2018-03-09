hallenge 4 - HDFS Testing

* Create the Issue `Test HDFS`
* Assign yourself and label it `started`
* As user `hilary`, use `teragen` to generate a 65,536,000-record dataset
  * Write the output to 16 files 
  * Set the block size to 64 MB
  * Set the mapper container size to 768 MiB
  * Name the target directory `tgen`
  * Use the `time` command to capture job duration
* Put the following in `challenges/labs/4_teragen.md`
  * The full `teragen` command and output 
```
```
  * The result of the `time` command
```
```

  * The command and output of `hdfs dfs -ls /user/hilary/tgen`
```
```

  * The command and output of `hadoop fsck -blocks /user/hilary`
```
```

* Push this work to GitHub and label the Issue `review`
* Assign the issue to the instructors
