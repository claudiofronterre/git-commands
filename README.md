# Introduction to Git

>  Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency. [Git web](https://git-scm.com/)

## Installation of git

Downloads for Mac OS X, Windows, Linux and Solaris can be found on the official web of [git - downloads](https://git-scm.com/downloads). Instructions to install Git for Linux, Mac and Windows, using these downloads, are described on the [Atlassian Documentation - Set up Git](https://confluence.atlassian.com/bitbucket/set-up-git-744723531.html).

#### Linux

For Debian/Ubunto distribution, use the next command to install Git:
```
sudo apt-get install git
```

If your linux distributions is other, find distribution-specific instructions on [Download for Linux and Unix](https://git-scm.com/download/linux).

Finally, you can check if Git has been installed with:
```
which git
# /usr/bin/git
```

#### Windows

1. Download the Git for Windows [installer package](https://git-scm.com/download/win).
2. Run the installer.
3. Select the location of the installation and proceed.
4. Select **Use Git from Bash only**.
5. Select **Checkout Windows-style, commit Unix-style line ending**.
6. Select **Use MinTTY**
7. Select **Enable ... **

Open **Git bash** on Programs directory to open a command window, if *java* is not recognized when typing `java` or `javac`:

Copy address of where binaries of java and javac are found (Program Files >> Java >> jdk >> bin) with semicolom on:

> windows >> control panel >> System and Security >> System >> Advanced System Settings >> Advanced >> Environment Variables >> Sytem variables >> Path

Open **Git bash** again and type `java`. It should be recognized now.

#### Mac

```
git --version
```
Download the Git installer from its official website.  
The installer is a DMG file. 
Double-click the DMG to expand it.
Double-click the PKG file to install it.
The Git installer launches.
Follow the prompts to install Git.
Open a terminal on your system.
Verify the installation was successful by typing which git --version at the command line.



> The easiest is probably to install the Xcode Command Line Tools. On Mavericks (10.9) or above you can do this simply by trying to run git from the Terminal the very first time. If you don’t have it installed already, it will prompt you to install it. [Install git on mac](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

```
Launch the App Store then download "Xcode".
Install Xcode, run it and go to Xcode’s preference via shortcut key `command` + `,`
Go to the Downloads tab, look for "Command Line Tools", and click Install.
quit and re-open Terminal, hit the git command and see if it has been successfully reinstated.
```

## Setting git and a web repository

### Linux

```
# Set up user.name for all the repositories.
git config --global user.name "Erick Chacon"

# Set up user.mail for all the repositories.
git config --global user.email "eral.th07@gmail.com"

# Check current user.name and user.email at once.
git config --list

# Check existing SSH keys.
ls -al ~/.ssh 
# public and private key pair listed (e.g. id_rsa.pub and id_rsa)

# Generate new SSH Key
ssh-keygen -t rsa -b 4096 -C "eral.th07@gmail.com"

# Adding SSH key to the ssh-agent.
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa

# Adding the new SSH key to GitHub account.
gedit ~/.ssh/id_rsa.pub # copy the content of the file
# Set a new SHH key on your GitHub settings.
```

### Windows

```
ssh-keygen -t dsa
cd ~/.ssh
ls -la
cat id_dsa.pub
git config --global user.name "Emma Paris"
git config --global user.email "eparis@atlassian.com"
```

## Git commands

### Clone a repository

### Create a branch

### Pull and push

### Merge branch with master repository

