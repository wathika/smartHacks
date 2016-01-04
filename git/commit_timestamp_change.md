####Changing commit timestamp

To change the timestamp on an old commit, use `git filter-branch` with an `env filter` that sets GIT_AUTHOR_DATE and GIT_COMMITTER_DATE for the specific hash of the commit you're looking to fix.

This will invalidate that and all future hashes.


For example If you wanted to change the dates of 
commit `119f9ecf58069b265ab22f1f97d2b648faf932e0`, you could do so with something like this:


```
git filter-branch --env-filter \
    'if [ $GIT_COMMIT = 119f9ecf58069b265ab22f1f97d2b648faf932e0 ]
     then
         export GIT_AUTHOR_DATE="Fri Jan 2 21:38:53 2009 -0800"
         export GIT_COMMITTER_DATE="Sat May 19 01:01:01 2007 -0700"
     fi'
```
