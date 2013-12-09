# pipe-logger

Ruby ~~Bash~~ script for easy log rotation and formatting

(Ruby version is 200x faster than the original bash version)

```sh
# 10MB * 10 (default)
chatty_process | pipe-logger chatty.log

# 100MB * 5
chatty_process | pipe-logger -s 100m -n 5 chatty.log

# With timestamp
chatty_process | pipe-logger -s 100m -n 5 -t chatty.log

# Standard output & error with process substitution
chatty_process > >(pipe-logger chatty.out) 2> >(pipe-logger chatty.err)
```

