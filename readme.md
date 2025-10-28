# Redirection

### _bash_
```bash
command > stdout 2> stderr 3> custom_file_descriptor
```
In the example above, if `command` has 4 file descriptors assigned to it (every command has at least 3), those are accessible at any point in this process.

In this case:
- 0 = stdin
- 1 = stdout
- 2 = stderr
- 3 = custom

These streams remain available until they are either replaced or discarded by another command down the line. Very cool!

By contrast, if you use a `|` to read the stdout stream, the stderr and custom streams will be discarded.
