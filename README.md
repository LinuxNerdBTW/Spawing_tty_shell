# SPAWING A TTY SHELL 
Often during pen tests you may obtain a shell without having tty, yet wish to interact further with the system. Here are some commands which will allow you to spawn a tty shell. Obviously some of this will depend on the system environment and installed packages.

* python -c 'import pty; pty.spawn("/bin/sh")'

* echo os.system('/bin/bash')

* /bin/sh -i

* perl —e 'exec "/bin/sh";'

* perl: exec "/bin/sh";

* ruby: exec "/bin/sh"

* lua: os.execute('/bin/sh')

 # (From within IRB)

* exec "/bin/sh"

# (From within vi)

* :!bash

# (From within vi)

* :set shell=/bin/bash:shell

# (From within nmap)

* !sh

# Making shell better or stable 
**eg**
* python3 -c 'import pty; pty.spawn("/bin/bash")';export TERM=xterm
* press ctrl + z on keyboard {background the current job on linux}
* stty raw -echo;fg [This is make your shell better for working]

