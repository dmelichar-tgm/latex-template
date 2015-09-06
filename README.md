LaTex Template
====================

This folder includes a LaTeX template which grants the basis for practically any document. It also includes a script which compiles the given ´document.tex´ file into a PDF in a neat manner. The only requirement for this to work is a functional LaTeX set up - for installation instructions see below.

Please note that *some* knowledge of (La)TeX is required



## Author(s)
- Daniel Melichr


## Table of contents
<!-- MarkdownTOC depth=0 -->

- [How to install LaTeX][Installation]
	- [Windows OS][Windows]
		- [TeXLive package - full version][TeXLive-Windows]
		- [Basic MikTeX - TeX  distribution][Basic-MikTeX-Windows]
		- [TeXStudio - TeX  editor][TeXStudio-Windows]
	- [Mac OS X][OSX]
		- [MacTeX - TeX  distribution][MacTeX-OSX]
		- [TeXStudio - TeX  editor][TeXStudio-OSX]
	- [Unix/Linux][Linux]
		- [TeXLive - TeX  distribution][TeXLive-Linux]
			- Getting the distribution:
			- Installation
			- For 32bit OS
			- For 64bit OS
			- Fedora/RedHat/CentOS:
			- SUSE:
			- Debian/Ubuntu:
- [Compiling a document][Compiling]
	- [Shell script for PDFLaTeX (Unix/Linux)][Shellscript]
	- [Using the batch file on Windows OS (PDFLaTeX)][Batchfile]

<!-- /MarkdownTOC -->

 


## How to install LaTeX [Installation]

### Windows OS [Windows]

#### TeXLive package - full version [TeXLive-Windows]

1.  Download the TeXLive ISO (2.2GB) from
    [https://www.tug.org/texlive/](https://www.tug.org/texlive/)

2.  Download WinCDEmu (if you don’t have a virtual drive) from
    [http://wincdemu.sysprogs.org/download/](http://wincdemu.sysprogs.org/download/)

3.  To install Windows CD Emulator follow the instructions at
    [http://wincdemu.sysprogs.org/tutorials/install/](http://wincdemu.sysprogs.org/tutorials/install/)

4.  Right click the iso and mount it using the WinCDEmu as shown in
    [ http://wincdemu.sysprogs.org/tutorials/mount/](http://wincdemu.sysprogs.org/tutorials/mount/)

5.  Open your virtual drive and run setup.pl


#### Basic MikTeX - TeX  distribution [Basic-MikTeX-Windows]

1.  Download Basic-MiKTeX(32bit or 64bit) from
    [http://miktex.org/download](http://miktex.org/download)

2.  Run the installer

3.  To add a new package go to Start >> All Programs >> MikTex >> Maintenance (Admin) and choose Package Manager

4.  Select or search for packages to install

#### TeXStudio - TeX  editor [TeXStudio-Windows]

1.  Download TexStudio from
    [http://texstudio.sourceforge.net/#downloads](http://texstudio.sourceforge.net/#downloads)

2.  Run the installer




### Mac OS X [OSX]

#### MacTeX - TeX  distribution [MacTeX-OSX]

1.  Download the file from
    [https://www.tug.org/mactex/](https://www.tug.org/mactex/)

2.  Extract and double click to run the installer. It does the entire configuration, sit back and relax.

#### TeXStudio - TeX  editor [TeXStudio-OSX]

1.  Download TexStudio from
    [http://texstudio.sourceforge.net/#downloads](http://texstudio.sourceforge.net/#downloads)

2.  Extract and Start




### Unix/Linux [Linux]

#### TeXLive - TeX  distribution [TeXLive-Linux]

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

## Compiling a document [Compiling]
### Shell script for PDFLaTeX (Unix/Linux) [Shellscript]

Usage: `sh ./compile.sh [OPTIONS]`

[option]  compile: Compiles the document

[option]  clean: removes temporary files

### Using the batch file on Windows OS (PDFLaTeX) [Batchfile]

*    Open command prompt and navigate to the directory with the tex file. Run:

    `compile-windows.bat`.

*    Alternatively, double click on `compile-windows.bat`
