### About
- Git is Directed acyclic graph
- short - continous improvement. stability,development branches. testing , quality through pull requests
- snapshort is an entire project. .Git contains staged and project history, objects etc
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

### commit messages
- must be in imperative active short detailed,Capitalized like ADD REMOVE etc
- donot end with period, summary only in commit, description in body

