# Regex - regular expression notes

## Notes

```bash
# go to root
cd /
```

- tail -> outputs the end of a file

Use `grep -E` for regex search

```bash
# always use single quote
grep -E 'root' passwd
```

### Regex special characters

# `*` -> matches zero or more times
grep -E 'Alexander'* passwd

# `+` -> matches one or more times
grep -E 'Alexander'+ passwd

# `{}` -> specifies how many times a character repeats
grep -E '[0-9]{4}' passwd

# `^` -> matches the beginning of a line
grep -E '^Alexander' passwd

# `[]` -> matches any one character inside the brackets
grep -E '[abc]' passwd

# `[^0-9]` -> When `^` is inside square brackets `[]`, it means NOT. Matches any character that is NOT a number between 0 and 9.
grep -E '[^0-9]' passwd


# `^[0-9]` -> When `^` is outside square brackets `[]`, it means the beginning of a line. Matches lines that START with a number between 0 and 9.
grep -E '^[0-9]' passwd

### /etc

directory for system config files -> applies to all users in the system
