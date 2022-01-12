## AutoInitialize Linux

# Purpose
To allow for a simple and fast install of all needed tools for Linux and initialize bash scripts.
This has been mainly tested on WSL Ubuntu.

# Running
1. Clone repo to local linux machine (run `git clone https://github.com/BenjaminMichaelis/Linux_AutoInitializeScript.git`)<br>
2. Navigate to repo location
3. Run the script you want (depending on permissions either `./initializelinux` or `bash initializelinux`
- Individual Scripts
  - `./setupgit` - for Git instillation
  - `./setupcpp` - for C/C++ compiling and debugging instillation
  - `./vsliveshare_prereqs` - for requirements for VSCode Liveshare.
- Platform Scripts
  - `./initializelinux` - for basic linux instillation
  - `./initialize_wsl2` - for basic linux instillation and x-display setup (#WIP)

# What is contained within each script?
Check out the [Notes](https://github.com/BenjaminMichaelis/Linux_AutoInitializeScript/blob/master/notes.md)
