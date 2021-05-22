# DollarSkip

## What is DollarSkip

DollarSkip is a short piece of C code designed to ignore the dollar symbol at the start of commands.

It aims to solve the annoyance of copying commands and having the annoying error

`$: command not found`

## Installation

### Automated install

You need wget installed
```
wget -qO- https://raw.githubusercontent.com/CleanMachine1/DollarSkip/master/install.sh | bash
```
### Manual install

You must be running Linux and have Git installed.

To install, run the following commands in a terminal:

```bash
cd ~/ # Or your place of choice for Git repos
git clone https://github.com/CleanMachine1/DollarSkip
cd DollarSkip
make #This makes the binary
sudo make install
make clean
```

After you can test to see if it works.

Open a terminal and run the command:

`$ echo 1`

If you get

`1`

it works!

If you get

`$: command not found`

please report an issue in the repo.

## Uninstallation

```bash
cd ~/DollarSkip
sudo make uninstall
cd .. 
sudo rm -r ./DollarSkip
```

## How this works

DollarSkip makes a binary file called $, in return whenever the first word of a command is $ on its own, Linux see this as a application, since when installing, the $ file is moved to /usr/bin

It can have side effects and if any occur, just run the uninstallation and tell me what went wrong!

## Side Note

This project was a learning experience for me, since my C needs to improve!

I am not responsible for any damage to your system!
max character count in a single command is 8000!
anything over may create a segmentation fault!

in no event shall the
authors or copyright holders be liable for any claim, damages or other
liability, whether in an action of contract, tort or otherwise, arising from,
out of or in connection with the software or the use or other dealings in the
software. (MIT license)

If you decided to run a stupid command which creates a buffer overflow, expect a system crash!
