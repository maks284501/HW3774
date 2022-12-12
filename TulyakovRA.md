# Instruction for work with GIT.
*Autor: Reggie188*\
**To all question write on: mr.tulyakov92@gmail.com**

## What is Git?

Git - version control system with distributed architecture.

## For what?

Git is used for version control by a huge number of software development projects, both commercial and open source.

## Installing Git.
### Mac OS:

**Open terminal and input next command:**\
*  git --version

If Git not instaled, it will prompt you to install it.

### Windows OS.

**First, must be installed libraries on which depends GIT: autotools, curl, zlib, openssl, expat и libiconv.**

You must use one is these command for installing all dependencies:\

* sudo dnf install dh-autoreconf curl-devel expat-devel gettext-devel 
* openssl-devel perl-devel zlib-devel

or this:

* sudo apt-get install dh-autoreconf libcurl4-gnutls-dev libexpat1-dev
* gettext libz-dev libssl-dev

For what collect documentation in various formats (doc, html, info), you will need to install additional dependencies:

* sudo dnf install asciidoc xmlto docbook2X
* sudo apt-get install asciidoc xmlto docbook2x

**If you're using a Debian OS, you must install packeg install-info:**

* sudo apt-get install install-info

**If you're using OS on base RPM, you must install packeg getopt:**

* sudo dnf install getopt

**Because of differenings names binary files you must input command:**

* sudo ln -s /usr/bin/db2x_docbook2texi /usr/bin/docbook2x-texi

**Next, download GIT from: https://github.com/git/git/releases:**

**Then compile and install:**

* tar -zxf git-2.8.0.tar.gz
* cd git-2.8.0
* make configure
* ./configure --prefix=/usr
* make all doc info
* sudo make install install-doc install-html install-info

### Lunix

**If you use Fedora (or another similar distribution such as RHEL or CentOS), you can use dnf:**

* sudo dnf install git-all

**If you use distribution such as Debian), you can use apt:**

* sudo apt install git

## Checking the correct installation

**For check that you correct installed Git  input this:**

* git --version (git version)

If you see on output git version, it means everything is fine.
Else, repead installing.

Bye!

## Additional settings.

### So! I'm continue adding instractions for work with Git.

### Git work ready. You can set it up to indicate the author when a commit is created.

*Installing name for our user*

* git config --global user.name "your_name"

*Now let's enter the mail*

* git config --global user.email "email@email.com"

## Create repositories.

### Let's create our first repository. To do this, go to your project folder

* cd <folder_repo>

* git init

### Git now tracks changes to your project files. And you need to create a commit.
### Or this, for adding all files
* git add --all

### Add specific file.
* git add <name_file>

### Now let's add a commit
* git commit -m "<commit_text>"

### Git procces work

* New functionality created
* Added a new block on layout
* Fixed bugs in code
* You want to close the working day and save the code



## Cloning an Existing Repository


To get a copy of an existing Git repository, such as a project that you want to contribute to, you need to use the command

### To get a copy of an existing Git repository, such as a project that you want to contribute to, you need to use the command:

* git clone 'rep path name'
#### or
* git clone -b branch_name 'rep path name'

### 
The git push command pushes all changes made by the user to a remote repository (for example, such as GitHub) during execution:

* git push 'remote_name' 'branch_name'

### The git pull command is responsible for downloading data from the server. The process is very similar to cloning a repository, but not all commits are downloaded here, only new ones.

* git pull 'remote repo'

### We also work with the project on the local machine, make changes, fix and save, and then we direct everything using:

- pull request


