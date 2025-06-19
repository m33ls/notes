Upgrade to an interactive shell
```sh
python3 -c 'import pty;pty.spawn("/bin/bash")'
CTRL-Z
stty raw -echo
fg
reset
export SHELL=bash
export TERM=xterm-256color
stty rows <num> columns <num>
```
