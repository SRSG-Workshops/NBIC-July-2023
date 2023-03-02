---
title: Setup for Computational Research Skills
---


# The Bash Shell

## Text Editor ##

A text editor is the piece of software you use to view and write code. If you
have a preferred text editor, please use it. Suggestions for text editors are,
Notepad++ (Windows), TextEdit (macOS), Gedit (GNU/Linux), GNU Nano, Vim.
Alternatively, there are IDE's (integrated developer environments) that have
more features specifically for coding such as VS Code; there are also IDEs
specific to languages will be listed in the appropriate section(s) below.

## Open a Terminal ##

For this lesson, first you need to be able to open a terminal:

- **On Windows:** run "Git Bash", to install git bash go here [https://gitforwindows.org/](https://gitforwindows.org/) click download and select 'Git-X.XX.X-64-bit.exe' from the assets list.
- **On Mac OS X:** accessed by opening the “Terminal” application, which can be found in the “Utilities” folder which is in your “Applications” folder.
- **On Linux:** this will depend on the Linux distribution you are running, but you should be able to find a "Terminal" application in your desktop's application menu.



## Git Setup ##

### Windows
We'll be using Git Bash for both git and a shell to run it in. If you've already installed Git Bash then go to the next section. Otherwise, go to [git for windows](https://gitforwindows.org/) and click **Download**, then install it. 
Most of the options can be left on default, but be sure you check these:

- **Choosing the default editor used by Git:** Make sure **Nano** is selected from the drop-down. If you're comfortable with other editors, feel free to change it, but we recommend Nano - we use it as it's present on Windows, Mac *and* Linux. If you change it, you might not quite match what we're doing on-screen.
- **Adjusting your PATH environment:** Make sure **Git from the command line and also from 3rd-party software** is selected.
- **Choosing HTTPS transport backend:** Make sure **Use the native Windows Secure Channel Library** is selected.
- **Configuring the terminal emulator to use with Git Bash:** Make sure **Use Windows' default console window** is selected.

#### Mac OS
To use Git you must install the Apple Command Line Tools, this may take a few minutes.  

You can obtain these [from Apple](https://developer.apple.com/download/more/?name=command%20line%20tools%20for%20xcode%2012) (requires your Apple ID)

- Select **Command Line Tools for Xcode 12 (or higher)** and click the link to download the dmg archive.
- If prompted, choose to allow downloads from developer.apple.com
- Open the downloaded dmg archive from the Downloads folder
- Double-click the Command Line Tools.pkg icon to install

Alternatively, you can install the tools from the command line:

~~~
$ xcode-select --install
~~~
{: .language-bash}

#### Linux
Git comes pre-installed on most Linux distributions. You can test if it's installed by running `git --version`. 
If it's not installed, you can install it by running `sudo apt-get install git` or `sudo yum install git`, depending on 
your distribution.


## GitHub ##
We'll be using the website [GitHub](https://github.com/) to host, back up, and distribute our code. You'll need to [create an account there](https://github.com/signup). As your GitHub username will appear in the URLs of your projects there, it's best to use a short, clear version of your name if you can.


## Download Data for Shell Lesson ##

Type the following into the prompt that appears (pressing enter/return after each line):

~~~
$ cd
$ git clone https://github.com/Southampton-RSG-Training/shell-novice.git
~~~
{: .language-bash}

`cd` will move to your home directory, and `git clone` will download a copy of the materials.

Alternatively, if you have SSH authentication with GitHub enabled (if you don't know what this means don't worry, it is covered in the Git SWC course if you want to know more!) you can use the following:

~~~
$ cd
$ git clone git@github.com:Southampton-RSG-Training/shell-novice.git
~~~
{: .language-bash}

This should download all the content for the lesson to a new directory.
Please let the instructors know if you run into any problems.

{% include links.md %}

# Version Control with Git

# Building Programs with Python

## Python Setup ##

IDEs: PyCharm, Spyder, VS Code

We use Python 3*. The “Anaconda3” package provides everything Python-related you will need for the workshop. 
To install [Anaconda](https://www.anaconda.com/products/individual), follow the instructions below.

Some old research projects may be in Python 2 but Python 2 has been retired and new projects should be in Python 3.

### Windows
Download the latest Anaconda Windows installer. Double-click the installer and follow the instructions. **When asked “Add Anaconda to my PATH environment variable”, answer “yes”. It will warn you not to, but it's required for it to be found by git bash** After it’s finished, close and reopen any open terminals to reload the updated PATH and allow the installed Python to be found.

Once the Anaconda installation is finished you will be asked if you want the installer to initialize Anaconda3 by
running conda init? You should select yes. Alternatively/additionally you will need to run the following command in 
GitBash

{: .bash}
~~~
conda init bash
~~~

Then close and reopen GitBash.

Please test the python install open GitBash (or your favorite terminal) and run the following command to verify that the installation was successful.

{: .bash}
~~~
cd ~
python
~~~

You can then type the following to exit:
{: .python}
~~~
quit()
~~~

{: .callout}
~~~
In some cases GitBash will hang on this command and not launch the Python interpreter. 
In this case close and reopen git bash and issue the following commands:
~~~

{: .bash}
~~~
cd ~
echo 'alias python="winpty python.exe"' >> .bashrc
source .bashrc
python
~~~


### Mac OS X

#### Mac OS Intel
Download the latest Anaconda Mac OS X installer. Double-click the .pkg file and follow the instructions.

#### Mac OS M1
If you have a M1 Mac you need a specific version of Anaconda follow the link below. 

[M1 Compatible Anaconda](https://repo.anaconda.com/archive/Anaconda3-2022.05-MacOSX-arm64.pkg)

Once the Anaconda installation is finished you will be asked if you want the installer to initialize Anaconda3 by
running conda init? You should select yes.

### Linux
Download the latest Anaconda Linux Installer.

Install via the terminal like this (you will need to change the version number to the latest version):

First move to the folder where you downloaded the installer, this is likely to be the Downloads folder e.g.

~~~
$ cd ~/Downloads
~~~
{: .language-bash}

~~~
$ bash Anaconda3-2021.11-Linux-x86_64.sh
~~~
{: .language-bash}

Answer ‘yes’ to allow the installer to initialize Anaconda3 in your .bashrc.

## Download Data for Python Lesson ##

Now we are ready to download the code that we need for this lesson. Open a terminal on your machine, and enter:
~~~
$ cd
$ git clone https://github.com/Southampton-RSG-Training/python-novice
~~~
{: .language-bash}

`cd` will move to your home directory, and `git clone` will download a copy of the materials.

{% include links.md %}

# Introductory Data Management with R

## Install R and RStudio ##

R is a programming language and software environment for statistical computing and graphics. The RStudio Integrated Development Environment (IDE) is a set of tools designed to help you be more productive with R.

We need to install R and RStudio: 
The latest links can be found on the [RStudio downloads page](https://www.rstudio.com/products/rstudio/download/#download)

### R

R can be found at [https://cran.rstudio.com/](https://cran.rstudio.com/), from here pick your OS and download the latest release, see below for direct links to your OS.

#### Windows
- [https://cran.rstudio.com/bin/windows/base/](https://cran.rstudio.com/bin/windows/base/)

#### Mac OS
- If prompted, choose to allow downloads from cran.rstudio.com.

- [https://cran.rstudio.com/bin/macosx/](https://cran.rstudio.com/bin/macosx/)
  - For intel based macs choose R-4.*.*.pkg
  - For ARM based macs (M1 etc.) choose R-4.*.*-arm64.pkg

#### Linux
- R is included on many linux distros check to see if it is already present. Else use your package manager (snap, apt, yum), or look [here](https://cran.rstudio.com/bin/linux/)


### RStudio

Your OS should be detected and a link provided under step 2 on this page [RStudio downloads page](https://www.rstudio.com/products/rstudio/download/#download).
Else select your OS from the list under All Installers.

#### Windows

Download and run the .exe file and follow instructions given by your OS.

#### Mac OS

Download the .dmg file.
- If prompted, choose to allow downloads from rstudio.com.
- Open the downloaded dmg archive from the Downloads folder.
- Drag the RStudio icon to the Applications folder to install.

#### Linux
Download the appropriate install file (.rpm or .deb) for your distro.