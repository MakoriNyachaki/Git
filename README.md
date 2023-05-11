## Git and Github

* Author: Makori Nyachaki

  Saving your code in a repository allows you to backup your code and showcase it to the world.

### Introduction

 * **Git** is a free and _open source distributed version control system_ designed to handle both
 small and very large projects with speed and efficiency. While **GitHub** is a _web-based_
 Git repository _hosting service_, and offers all of the _distributed revision control_ and
 _source code management (SCM)_ functionality of Git and also implements other new features.

**Version Control System**

 * Keeps track of changes in your files.
 * Helps one collaborate with others on various projects.
 * Tests changes without losing original versions.
 * Ease to revert to previous versions if needed.

**Web-based hosting service for git**

 * Provides a "remote" workplace for yor git workplaces.
 * Acts as backup incase of theft and breakdown.

### Installing Git

**Linux Users**

 * Checking the version and if git is installed
	git --version
 _if it is installed it returns the version of git installed_
 _If you are using a RedHat style distribution (RedHat, CentOS or Fedora), type_

	sudo yum -y install git
 or their newer versions

	sudo dnf -y install git
 and if you are using Debian-based distributions i.e. Ubuntu

	sudo apt-get git

**Mac Users**

Download git bash package for macs from [here](https://git-scm.com/download/mac)

_Remember to follow instruction on the page._

**Windows Users**

 * [Go to](https://git-scm.com/download/win) and download git for windows.
 * Follow the steps [here...](https://www.geeksforgeeks.org/how-to-install-git-on-windows-command-line/) to install and configure.

### Configuring Git

Great! You have successfully installed Git. It is time to let Git know who you are.
This is very important because each commit uses this information on any VCS.
All this is done in your commandline.

 * Configuring your username
	git config --global user.name "Your name"
 * Configuring your email
	git config --global user.email "Your Email"

**_Note:_** The _global_ is used to set the username and email for every repository in your account.
Otherwise you can remove _global_ flag to set a username and email for each repo each time you use it.


### Creating and Initializing Git folder

While on your terminal navigate to a specific location where you want to create your folder using the **cd** command:
Then create a folder using the following command:
	mkdir foldername

To navigate into your folder use the _cd_ command i.e.
	cd foldername

After creating and you are in your folder initialize your folder using:
	git init

 * _mkdir_ - makes a new directory(make directory)
Syntax: _mdir dirctoryname_

 * _cd_ - Change current working directory(Change directory)
Syntac: _cd directoryname/path_to_you_target_directory_

 * Initializing a directory git creates a hidden(.init) folder which it uses to track changes in the main directory.

### Create a New File

 Now in your git repository create a new file using your available text editors.
 Example: Create _hello.c_ with the following contents:
	
	#include <stdio.h>

	/**
	* main -Entry point
	* Return: 0
	*/
	int main(void)
	{
		printf("Hello World, I am learning Git");

		return (0);
	}

### Staging the File

Staging means signals git to track changes in a file. It is done through the following command:
Syntax: _git add filename_ 
The file name in our case is 'hello.c'
	git add hello.c

Incase you have many file you can use '-A' or '--all' flags to track changes in all files.
'-A' flag is a shorthand of '--all' and serve the same purpose. Usage

	git add -A

or

	git add --all

You can also use the dot(.) to track changes in all files. Usage:
	git add .

### Git Commit

We are now set to keep track of our changes on git using _git commit_.
Each commit is considered as a saving point in Git.

Syntax: _git commit -m "commit message"

**Note:** The commit message should relate with what you have done to your project with regrad to your previous work.

Example committing our staged file:
	git commit -m "First implementation of hello world"

 * Sometimes you can commit without staging a file. This is so especially when changes are very small.
 * This is achieved using **-a** flag which will stage every change automatically in every file. Usage:

	git commit -a -m "Added a  new line to hello world"

### Git Status

Syntax: git status

Displays useful information about your repository (e.g., current branch, tracked/untracked files,
differences between local and remote versions)

**Note:** Short status flags are:

    ?? - Untracked files

    A - Files added to stage

    M - Modified files

    D - Deleted files

It has got other options too like --short, ...

### Git Push

This uploads all local commits to remote i.e from your computer to Github.
Command:
	git push


### Git Log

Used for viewing the history of commits of your repository.
Command is:
	git log

### Git Branch
