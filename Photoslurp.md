this repo is a fork of github.com:h2non/imaginary.git
it is needed to be updated from the forks work sometimes. below is the guide to do that.
## to update
add source of fork if not added to your local repo first:
```
$ git remote add source git@github.com:h2non/imaginary.git
```
verify it is there;
```
$ git remote -v
origin	git@github.com:photoslurporg/imaginary.git (fetch)
origin	git@github.com:photoslurporg/imaginary.git (push)
source	git@github.com:h2non/imaginary.git (fetch)
source	git@github.com:h2non/imaginary.git (push)
```
now you have the forked (original) version under source/

fetch it:
```
git fetch source
```

checkout to develop branch:
```
git checkout develop
git rebase source/master
```

i prepeared a diff file to apply over the changes. since the source file can be changed in a way that can not be done automatically. it is usefull to apply them line by line if necessary (if rebase not works)

the diff file is `/pslurp_changes.diff`

when rebase is done or the diff is applied `git apply pslurp_changes.diff` then it is ready to be built.

follow makefile's commands to build. that's all.
