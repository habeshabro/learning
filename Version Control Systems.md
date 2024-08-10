## Definition
	Version Control Systems, VCSs for short, are a tool used to keep track of the changes made to files so that: 
	1) We can "go back in time" and get older versions of the files 
	2) We can "create parallel universes" where different versions of the same file can exist at the same time
	3) We can observe all the changes that have been made through time
	4) See who made what changes 

## Types of VCSs

### a) No VCS
		When there are no VCSs, people had to make do with simply remembering changes in their minds or copying older versions of their files in another directory by simplying copying it there, maybe by keeping them in timestamped files. Both methods suffer from the same flaw, the human component. People forget stuff.

### b) Local Version Control Systems
	These systems had simple databases that kept track of all the changes done to a file, automating the previous process. Examples: 
- [[RCS]] : A Local VCS that stores patch sets(or deltas) in a special format on a disk 

### c) Central Version Control Systems
	The need to collaborate on projects made it necessary to move the repo to a central server. The users would have the ability to checkout any version they want from this central server. Examples: 
	- CVS
	- Subverse
	- Perforce

### d) Distributed Version Control Systems
	These systems are different from CVCSs in one critical way, the users don't just checkout a single version from the central server, they mirror the entire repo, taking all the history and versions to local storage. Examples:
- [[GIT]]
- Mercurial
- Darcs
 