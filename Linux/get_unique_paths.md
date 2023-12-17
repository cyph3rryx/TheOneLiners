```bash
curl https://www.inlanefreight.com/ | grep -Eo "https:\/\/.{0,3}\.website\.com[^\"\']*" | sort -u | wc -l
```

This command is using `curl` to fetch the main website, then `grep` with the `-Eo` option to extract all the paths that start with `https://`, followed by up to 3 characters, then `.website.com`, and finally end with any character except `"` or `'` (which is what `[^\"\']*` means). The `sort -u` command is used to sort the paths and remove duplicates, and `wc -l` is used to count the number of lines.

This command will give you the number of unique paths that match the specified pattern.
