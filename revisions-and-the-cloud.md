
### Wednesday, April 29th

**Revisions and the Cloud**

Let's begin with a data dump of terms:

|Term|Definition|
|:--|--:|
|Local Version Control|A single database on your hard disk that stores changes to files|
|Centralzied Version Control|A single server that stores all changes and file versions and can be accessed by various clients|
|Distributed Version Control|Allows clients to create mirrored repositories, addressing the vulnerability of the CVS as a single failure point|

Which brings us to a major topic when discussing revisions and the cloud... ***Git***.

Git is a DVC that was developed in 2005 and remains one of the most utilized version control systems in the world.  So how does it work?

Git is essentially a file system that tracks changes made to your project in a series of snapshots.  Each snapshot represents a saved version of your project along the way - also called a *commit*.  These files can exist in one of three states:

1. **Modified**: changed, but not yet committed to the database
1. **Staged**: a change has been flagged to be committed during the next snapshot
1. **Committed**: stored to a local database

So what does this all *mean*?

In the simplest possible terms, Git is DVC which means it allows you to work on a project remotely by creating a clone of the original project and tracking all changes made to that clone.  When you've made changes that you are happy with and want those changes to be added to the original project - not just your local clone - Git is able to look at the changes you've made and facilitates "committing" those changes to the original (origin) project.  This can be accomplished through three simple commands:

1. git add *filename*: identifies which file we want to commit.
1. git commit -m "*commit message*": confirms that we are committing the file identifed in step 1, and attaches a commit message that we can use note what we changed and why.
1. git push origin master: actually *pushes* that commited file from the master (local) repository to the origin(original) server, where those changes will now be reflected.

This chain of commands - add, commit, & push - can colloquially be refered to as the '*git flow*'.





[Home](https://jchinzi.github.io/learning-journal/)
