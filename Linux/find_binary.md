```bash
find /usr/bin /usr/sbin /usr/local/bin /usr/local/sbin -type f -exec getcap {} \;
```

This one-liner uses the find command to search for all binary executables in the directories where they are typically located and then uses the -exec flag to run the getcap command on each, showing the capabilities that have been set for that binary. The output of this command will show a list of all binary executables on the system, along with the capabilities that have been set for each.
