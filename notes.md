# Notes:
- [Table of Contents:](#notes)
  - [Script Creation Notes](#script-creation-notes)
    - [To convert script to unix if it is not running properly](#to-convert-script-to-unix-if-it-is-not-running-properly)
    - [Single Line Commants](#single-line-commants)
    - [Apt commands](#apt-commands)
  - [Script Commands Details](#script-commands-details)
    - [Start:](#start)
    - [C/C++ Compiling:](#cc-compiling)
    - [Git:](#git)
    - [Debugger:](#debugger)
    - [To compile C programs into 32-bit code in 64-bit Ubuntu Linux: (for CPTS-360) (command: cc -m32 'filename')](#to-compile-c-programs-into-32-bit-code-in-64-bit-ubuntu-linux-for-cpts-360-command-cc--m32-filename)
    - [Potential helpful software for CPTS 360?](#potential-helpful-software-for-cpts-360)
    - [Install xclip to copy SSH Keys](#install-xclip-to-copy-ssh-keys)
    - [Not working yet/ #TODO](#not-working-yet-todo)
## Script Creation Notes
### To convert script to unix if it is not running properly
This is a problem when you write script in windows with line endings, etc. (more info: https://askubuntu.com/questions/979213/cant-apt-get-from-shell-script)<br>
Run following command in terminal
```
sed -i -e 's/\r$//' initializelinux
```
Then try
```
./initializelinux
```
### Single Line Commants
You can put multiple commands in one line like:
```
sudo apt-get install build-essential gdb git
```
This would install build-essential, gdb, and git
or also:
```
sudo apt-get update && sudo apt-get dist-upgrade
```
### Apt commands
`-qq` suppresses output unless an error occurs
`--yes` answers the prompt 'Do you want to continue? [Y/n]'

## Script Commands Details
### Start:
To update the distribution:
```
sudo apt-get update
```
To update latest versions of system packages: 
```
sudo apt-get dist-upgrade
```
To install stuff from internet and have certificates for following command(two commands):
```
sudo apt-get install wget ca-certificates
```
Reference for following command: https://docs.microsoft.com/en-us/visualstudio/liveshare/reference/linux#install-linux-prerequisites
```
wget -O ~/vsls-reqs https://aka.ms/vsls-linux-prereq-script && chmod +x ~/vsls-reqs && ~/vsls-reqs
```
```
sudo apt install libssl1.0.0 libkrb5-3 zlib1g libicu[0-9][0-9] gnome-keyring libsecret-1-0 desktop-file-utils x11-utils
```

### C/C++ Compiling:
```
    sudo apt-get install gcc
    sudo apt-get install g++
```
### Git:
```
    sudo apt-get install git
```
### Debugger:
```
    sudo apt-get install ddd
    sudo apt-get install build-essential 
    sudo apt-get install gdb
```
### To compile C programs into 32-bit code in 64-bit Ubuntu Linux: (for CPTS-360) (command: cc -m32 'filename')
```
    sudo apt-get install gcc-multilib
```
### Potential helpful software for CPTS 360?
    sudo apt install emacs

### Install xclip to copy SSH Keys
    

### Not working yet/ #TODO
    Install Snapd: manages and maintains packages (needed for snapd commands)
        sudo apt update
        sudo apt install snapd
    
    Install VSCode

    Forward display
        need to run and install xLaunch
        export DISPLAY="`grep nameserver /etc/resolv.conf | sed 's/nameserver //'`:0"

    looks intersting
        sudo apt-get install tasksel
