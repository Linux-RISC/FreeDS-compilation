<a href="https://www.buymeacoffee.com/rbpiuserf" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>
<br>
Last update: 2022/12/02<br>
<br>
# FreeDS-compilation
Compilation process for FreeDS<br>
<br>
This works for me:<br>
<br>
Development system installation for Windows:<br>
<br>
install VSCodium (optional, you can use any editor, https://github.com/VSCodium/vscodium/releases)<br>
install Python (https://www.python.org/downloads/release/python-3110/)<br>
install platformio: python get-platformio.py, download from https://raw.githubusercontent.com/platformio/platformio-core-installer/master/get-platformio.py<br>
install git (https://git-scm.com/download/win)<br>
download source code: git clone https://github.com/pablozg/freeds.git<br>
add to PATH %USERPROFILE%.platformio\penv\Scripts using the editor of environment variables<br>
compilation: enter into freeds directory using CMD and run "pio run"<br>
generate the file system: enter into freeds directory and run "pio run --target buildfs"<br>
<br>
Tested on Debian GNU/Linux 11.5 amd64:<br>
$ sudo apt install python<br>
<br>
$ wget https://raw.githubusercontent.com/platformio/platformio-core-installer/master/get-platformio.py<br>
<br>
$ sudo apt install python3-venv<br>
<br>
$ python3 get-platformio.py<br>
<br>
$ sudo apt install git<br>
<br>
$ git clone https://github.com/pablozg/freeds.git<br>
<br>
$ cd freeds<br>
<br>
Compilation:<br>
$ $HOME/.platformio/penv/bin/pio run<br>
$ $HOME/.platformio/penv/bin/pio run --target buildfs<br>
<br>
You can also modify the file .profile of your user:<br>
PATH=$PATH:$HOME/.platformio/penv/bin<br>
<br>
and compile:<br>
$ pio run<br>
$ pio run --target buildfs<br>
<br>
Credits: svcabre and Linux-RISC<br>
