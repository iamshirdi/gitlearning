### About
- Git commit history is Directed acyclic graph
- short - continous improvement. stability,development branches. testing , quality through pull requests
- snapshort is an entire project. .Git directory contains staged and project history, objects etc
- Git commits point to their parent commits
- HEAD -> master
HEAD is a reference to the current commit.master is the name of the branch, and this
commit is the tip of the branch, so this is the master branch label. The arrow represents that
the HEAD reference points to the master branch label, which points to the SHA-1 of the
commit. Head points to symolic reference of master
- Merge occurs when commit has more than one parent and branch vice versa 
B (branch)
           D (Merge)  arrow points from d to b and c where D is latest commit
C (branch)
- git objects are commit,annotation,tree,blob
- git id name of git object 40 hexa decimal string(avalanche) also shorten git id
- Tilde(~ ~) refers to parent A<-B<-C where C is latest
- Caret (^ same as parent ^2 points to two parents only occurs when there is merge) refers to parent of merge commit
- Lightweight git tag v0.1 . Tags must be pushed git push remote name  tagname or --tags for all
- Annotated git tag -a -m "" or without m editor pops up similar to command. has author information signing etc and also an object

### Installation
- git config user.name 
- git config core.editor .

### Remote
- git remote -v to display remote information
- git remote add name (origin) url(usually ends with .git) short hand reference as origin
- git push -u(tracks changes) origin(repository name short hand reference can use or url) branch name (default master) 

### Branch,Merge
- git log --oneline --graph --all . Add --all shows all of the local branches instead of default branch you are currently on.
- git checkout sha-1(detached head) and git checkout -b auto create instead of git branch branchlabel 
- git branch for all list branches and git branch -d branchlabel to delete
- The -D will let you delete even if unmerged commits are present. only feature label deleted the dangling commits are later garbage collected by git automatically
- The default fast forward merge can be overwritten by git merge --no-ff feature3 (some companies etc require the merge branch to be displayed- non linear history)
- checkout to branch and then merge the branch u want to within this branch can view graphicall using online graph of current branch
- git merge --abort to merge/abort changes
- origin/master label represents the tip of the tracking branch that tracks the master
branch on the remote repository.
- master local repository tip
- origin/HEAD label represents the tip of the default branch on the remote repository.
The default branch on the remote repository is the master branch

### Rewriting history
- git commit --amend -m "message here" will change/(overwrite files) and the sha commit compared to previous
- git rebase -i sha1 (parent commit) to edit/perform actions like delete,squash,pick,edit on its children
- git merge --squash feature2 while checking out master to squash(single commit instead of multiple commits of branch) the merge. git commit if want  to add message
- rebase -i is performed on same branch unlike rebase
- git checkout feature and git rebase master to rebase feature commit to tip of master branch(feature branch have master files in working directory now easy fast forward master branch due to same ancestor). git rebase--continue after fixing the staged conflict files
 
### pull requests
- pull request can be created  without commits when creating branch to track,or any changes made with ultimate goal of merging after reviews/feedback by peers
- forking(can alsobe used for testing,opensource etc) does not read write permission on original true source of truth repository. can pull request and the owner can perform the merge
- forking(remote) sync needs to perform everytime manually(onto upstream) if u want to pull etcc or be to update. may invovole multiple remote repositroies
- centralized workflow cannot make use of branches,pull requests:discussions,mreges not good practice
- feature branch workflow should be prefered over centralized like dev,production. most of work done topic branches
- Some common practices of gitworkflow(allows work to be done even if they are hotfix in production,devs) are adding testing dev before adding to production hotfixing production and replicate the fixes in dev too. merge occurs only after these steps no direct merge between dev and production


### commit messages
- must be in imperative active short detailed,Capitalized like ADD REMOVE etc
- donot end with period, summary only in commit, description in body

