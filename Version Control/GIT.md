## Introduction

	Git is a distributed version control system. Some of its most important features are:
	- it uses snapshots, not differences: This means that every time a file is commited, if there is a change then it saves a snapshot of the whole file and if there are no changes, it saves a link to the previous version of the file to avoid redundancy
	- most of the opoeration are local
	- it uses checksum(SHA1) to enforce integrity: it even uses these tags to save stuff
	- very rarely deletes data: most operartions just add data

## How it Works

	There are three areas of interest:
	- Working area/tree: This is the main area where the user actively works on files. When a user makes a change to a file, it state changes to **modified**. Then the user can stage the changes and that sends the changes to the:
	- Staging area: This is a special part of the .git directory that housed the staged files that the user specifically wants to commit. In this area the files are marked as **staged**
	- .git directory/ repo: this is the area where all the commited changes live. It is what is copied when a project is cloned

[[GIT commands]]