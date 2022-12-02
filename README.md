# FreeDS-compilation
Compilation process for FreeDS

This works for me:

Development system installation for Windows:

install VSCodium (optional, you can use any editor, https://github.com/VSCodium/vscodium/releases)
install Python (https://www.python.org/downloads/release/python-3110/)
install platformio: python get-platformio.py, download from https://raw.githubusercontent.com/platformio/platformio-core-installer/master/get-platformio.py
install git (https://git-scm.com/download/win)
download source code: git clone https://github.com/pablozg/freeds.git
add to PATH %USERPROFILE%.platformio\penv\Scripts using the editor of environment variables
compilation: enter into freeds directory using CMD and run "pio run"
generate the file system: enter into freeds directory and run "pio run --target buildfs"
Tested on Debian GNU/Linux 11.5 amd64:
$ sudo apt install python

$ wget https://raw.githubusercontent.com/platformio/platformio-core-installer/master/get-platformio.py

$ sudo apt install python3-venv

$ python3 get-platformio.py

$ sudo apt install git

$ git clone https://github.com/pablozg/freeds.git

$ cd freeds

Compilation:
$ $HOME/.platformio/penv/bin/pio run
$ $HOME/.platformio/penv/bin/pio run --target buildfs

You can also modify the file .profile of your user:
PATH=$PATH:$HOME/.platformio/penv/bin

and compile:
$ pio run
$ pio run --target buildfs

Credits: svcabre and Linux-RISC
