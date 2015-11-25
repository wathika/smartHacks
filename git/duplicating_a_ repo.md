####Duplicating a repository

To create a duplicate of a repository without forking, you need to run a special clone command against the original repository and mirror-push to the new one.

In the following cases, the repository you're trying to push to--like `exampleuser/new-repository` or `exampleuser/mirrored`--should already exist on GitHub.

####Mirroring a Repo

you need to perform both a bare-clone and a mirror-push.

```
$ git clone --bare https://github.com/exampleuser/old-repository.git
# Make a bare clone of the repository

$ cd old-repository.git
$ git push --mirror https://github.com/exampleuser/new-repository.git
# Mirror-push to the new repository

$ cd ..
$ rm -rf old-repository.git
# Remove our temporary local repository
```