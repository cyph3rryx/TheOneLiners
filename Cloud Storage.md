## Find buckets and sensitive data

```
site:s3.amazonaws[.]com "target[.]com"
site:blob.core[.]windows[.]net "target[.]com"
site:googleapis[.]com "target[.]com"
site:drive[.]google[.]com "target[.]com"
```


### Can be combined the following terms with the Dorks:

```
site:s3.amazonaws[.]com | site:blob.core[.]windows[.]net | site:googleapis[.]com | site:drive[.]google[.]com "target[.]com"
```

- Add something to narrow the results: "confidential” “privileged" “not for public release”
