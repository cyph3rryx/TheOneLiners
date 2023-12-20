``` bash
find /path/to/search -type f -name "*.txt" | xargs grep "keyword" | sort -u > result.txt```
```

### A versatile text search and sorting tool for files. 
- It efficiently locates all text files with a .txt extension in a specified directory and its subdirectories.
- Subsequently, it searches for a user-defined keyword within these files, sorts the results alphabetically, removes duplicates, and finally saves the unique sorted output to a file named "result.txt."
