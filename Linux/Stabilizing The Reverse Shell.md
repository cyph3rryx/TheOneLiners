```bash
python3 -c 'import pty; pty.spawn("/bin/bash")'
```
This is a Python command that spawns a new interactive bash shell. It does this by importing the `pty` module, which provides a pseudo-terminal, and then using the `spawn` function to execute the `/bin/bash` shell. This is often used in reverse shells to gain a more stable and interactive shell.
