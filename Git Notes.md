# Git Notes

## Getting Info

___git remote update___ will update all of your branches set to track remote ones, but not merge any changes in.

___git fetch___ will update only the branch you're on, but not merge any changes in.

___git pull___ will update and merge any remote changes of the current branch you're on. This would be the one you use to update a local branch.

## Feature Complete ##
~~~
git branch -d feature/ahm_181704  <-- Freindly delete -d
git branch -D feature/ahm_181704  <-- Force delete -D
~~~

~~~
git flow init -d  
git stash
git pull
git flow init -d
git pull
git flow feature start myFeature
git checkout feature/myFeature
git push
~~~

## Git Large File Storage (LFS)
~~~
git lfs logs last
~~~

## Logs
~~~
git log --graph
git log origin/develop
~~~

## Tags
~~~
git push origin --tags
~~~

## Diff
~~~
git diff --stat origin/master
~~~

## Local Branches

command | description
------- | -------------
git branch --merged | List of 'merged' branches'
git branch --no-merged | List of 'not merged' branches

## References to remote branches
command | description
------- | -------------
git branch -r | List referenced remote branches
git remote prune origin | Clean-up outdate references
git fetch -p | Git automaticlly prunes all stale references

## Detail of merged remote
~~~
 for branch in `git branch -r --merged | grep -v HEAD`; do echo -e `git show --format="%ci %cr %an" $branch | head -n 1` \\t$branch; done | sort -r
~~~

## Detail of not merged remote
~~~
for branch in `git branch -r --no-merged | grep -v HEAD`; do echo -e `git show --format="%ci %cr %an" $branch | head -n 1` \\t$branch; done | sort -r
~~~

## Git Diff Between Branches
~~~
git diff mybranch master -- myfile.cs
~~~

## Git Stash
- [Useful tricks you might not know about Git stash](https://medium.freecodecamp.org/useful-tricks-you-might-not-know-about-git-stash-e8a9490f0a1a) Srebalaji Thirumalai Jan 26, 2018  
  - git stash save “Your stash message”.
  - git stash save -u  
      or  
    git stash save --include-untracked  
  - git stash list  
  - git stash apply stash@{1}  
  - git stash pop stash@{1}  
  - git stash show -p  
  - git stash show stash@{1}  
  - git stash branch <name> stash@{1}  
  - git stash drop stash@{1}  
  - 


