This repository contains scripts and rules used to convert the BOINC SVN
repository to Git.

The core of the conversion is the 'boinc-rules' file for [svn2git](http://gitorious.org/svn2git/svn2git/),
and the associated account-map.

To-do
-----

* **Add the rest of the version branches**, there's only up to 6.6a at the moment.
  Note: 6.8 seems to have its own complexities that I will have to check
  individually.
* **Add release tags**.
* **Complete the account-map**. There's several more names and addresses that I
  can take from Oliver's boinccleaned.git.
* **Remove binary files from version branches**. Currently they are only
  removed from trunk, but the branches have a lot of them too.
* **Fix weird merges and deletions from cvs2svn**. In many cases, there are copies
  from trunk to branch (which svn2git converts as git merges) immediately
  followed by deletions of those same files from the branch (?!). I should
  filter those out completely.
