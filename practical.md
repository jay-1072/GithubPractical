## Rebase Practicle

* To rebase feature branch commits

    * git checkout \[feature-branch\]

    * git rebase -i \[Master-branch\]

    * git checkout \[master-branch\]

    * git rebase -i \[feature-branch\]

    * git push origin master

## Change commit message

* To change latest commit message

    * git commit --amend -m 'Changed message'

* To change any commit message

    * git rebase -i HEAD~x  
	(x  being a number. 1 going back one more, 2 going back two more, etc.)
	
	Above command will open editor type reword inplace of pick
    Again new editor will open change the message and close editor

* To change very first commit / Initial commit message

    * git rebase -i --root

    do the same as above

## cherry pick

* To cherry pick

    * git checkout \[master-branch\]

    * git cherry-pick  \[Commit id of feature branch\]

    It will create new commit in master branch

* To cherry pick more than one commit

    * git cherry-pick \[Commit id 1\] \[Commit id 2\] …

* To avoid creating commit while doing cherry pick

    * git cherry-pick  \[Commit id of feature branch\] -n
    -n for no committing, above command will stage the commit of feature branch

## drop commit

* To drop commit First reset HEAD to parent commit

    * git reset \[Parent commit id\]

    After executing this command HEAD will point to parent commit

* To reflect changes on remote branch / To delete commit on Remote repository

    * git push origin \[Branch Name\] -f

     -f means force fully.

* If we want that commit again then we can get that using commit id
	* git cherry-pick \[commit id\]
