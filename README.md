LaTex Template
====================

This folder includes a LaTeX template which will probably be used for a lot things in the upcoming year. It also includes a script which compiles the given .tex file into a PDF in a neat manner. The only requirement for this to work is a functional LaTeX set up - for installation instructions see below.

Please note that *some* knowledge of (La)TeX is required



## Author(s)
- Daniel Melichr

## Table of Contents
- [How to install LaTeX]
    - [Windows OS]
        - [TeXLive package - full version])
        - [Basic MikTeX - TeX  distribution]
        - [TexStudio - TeX  editor]
    - [Mac OS X]
        - [MacTeX - TeX  distribution]
        - [TexStudio - TeX  editor]
    - [Unix/Linux]
        - [TeXLive - TeX  distribution]
            - [Getting the distribution]
            - [Installation]
            - [For 32bit OS]
            - [For 64bit OS]
            - [Fedora/RedHat/CentOS]
            - [SUSE]
- [Information regarding the template]
    - [Compiling a TeX ]
        - [Shell script for PDFLaTeX (Unix/Linux)]
        - [Using the batch file on Windows OS (PDFLaTeX)]  


## How to install LaTeX

### Windows OS

#### TeXLive package - full version

1.  Download the TeXLive ISO (2.2GB) from
    [https://www.tug.org/texlive/](https://www.tug.org/texlive/)

2.  Download WinCDEmu (if you don’t have a virtual drive) from
    [http://wincdemu.sysprogs.org/download/](http://wincdemu.sysprogs.org/download/)

3.  To install Windows CD Emulator follow the instructions at
    [http://wincdemu.sysprogs.org/tutorials/install/](http://wincdemu.sysprogs.org/tutorials/install/)

4.  Right click the iso and mount it using the WinCDEmu as shown in
    [ http://wincdemu.sysprogs.org/tutorials/mount/](http://wincdemu.sysprogs.org/tutorials/mount/)

5.  Open your virtual drive and run setup.pl

or

#### Basic MikTeX - TeX  distribution

1.  Download Basic-MiKTeX(32bit or 64bit) from
    [http://miktex.org/download](http://miktex.org/download)

2.  Run the installer

3.  To add a new package go to Start >> All Programs >> MikTex >> Maintenance (Admin) and choose Package Manager

4.  Select or search for packages to install

### TexStudio - TeX  editor

1.  Download TexStudio from
    [http://texstudio.sourceforge.net/#downloads](http://texstudio.sourceforge.net/#downloads)

2.  Run the installer




## Mac OS X

#### MacTeX - TeX  distribution

1.  Download the file from
    [https://www.tug.org/mactex/](https://www.tug.org/mactex/)

2.  Extract and double click to run the installer. It does the entire configuration, sit back and relax.

#### TexStudio - TeX  editor

1.  Download TexStudio from
    [http://texstudio.sourceforge.net/#downloads](http://texstudio.sourceforge.net/#downloads)

2.  Extract and Start




## Unix/Linux

#### TeXLive - TeX  distribution

##### Getting the distribution:

1.  TexLive can be downloaded from
    [http://www.tug.org/texlive/acquire-netinstall.html](http://www.tug.org/texlive/acquire-netinstall.html).

2.  TexLive is provided by most operating system you can use (rpm,apt-get or yum) to get TexLive distributions

##### Installation

1.  Mount the ISO file in the mnt directory
```sh
    mount -t iso9660 -o ro,loop,noauto /your/texlive****.iso /mnt
```

2.  Install wget on your OS (use rpm, apt-get or yum install)

3.  Run the installer script install-tl.
```sh
    cd /your/download/directory
    ./install-tl
```

4.  Enter command ‘i’ for installation

5.  Post-Installation configuration:
    [http://www.tug.org/texlive/doc/texlive-en/texlive-en.html#x1-320003.4.1](http://www.tug.org/texlive/doc/texlive-en/texlive-en.html#x1-320003.4.1)

6.  Set the path for the directory of TexLive binaries in your .bashrc file

##### For 32bit OS

For Bourne-compatible shells such as bash, and using Intel x86 GNU/Linux and a default directory setup as an example, the file to edit might be
```sh
    edit $~/.bashrc file and add following lines
    PATH=/usr/local/texlive/2011/bin/i386-linux:$PATH; 
    export PATH 
    MANPATH=/usr/local/texlive/2011/texmf/doc/man:$MANPATH;
    export MANPATH 
    INFOPATH=/usr/local/texlive/2011/texmf/doc/info:$INFOPATH;
    export INFOPATH
```
##### For 64bit OS
```sh
    edit $~/.bashrc file and add following lines
    PATH=/usr/local/texlive/2011/bin/x86_64-linux:$PATH;
    export PATH 
    MANPATH=/usr/local/texlive/2011/texmf/doc/man:$MANPATH;
    export MANPATH 
    INFOPATH=/usr/local/texlive/2011/texmf/doc/info:$INFOPATH;
    export INFOPATH
```
##### Fedora/RedHat/CentOS:
```sh
    sudo yum install texlive 
    sudo yum install psutils 
```
##### SUSE:
```sh
    sudo zypper install texlive
```
##### Debian/Ubuntu:
```sh
    sudo apt-get install texlive texlive-latex-extra 
    sudo apt-get install psutils
```

## Compiling a TeX
### Shell script for PDFLaTeX (Unix/Linux)

Usage: `sh ./compile-thesis.sh [OPTIONS] [filename]`

[option]  compile: Compiles the PhD Thesis

[option]  clean: removes temporary files - no filename required

### Using the batch file on Windows OS (PDFLaTeX)

*    Open command prompt and navigate to the directory with the tex file. Run:

    `compile-thesis-windows.bat`.

*    Alternatively, double click on `compile-thesis-windows.bat`
