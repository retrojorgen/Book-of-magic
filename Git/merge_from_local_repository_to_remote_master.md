Scenario:

I have a repository called "blabla".
I have a remote master,
local master that pulls from the remote master,
and a local branch called "somethingsome".

1. Push local commits to somethingsome to remote.
    git push origin master:somethingsome to create remote repo.
    git push origin somethingsome.

2. Run git fetch --all to make sure you are up to date.

3. Run git status to see if there are any changes that
haven't been committed.

3b. If there are any changes, amend them.
    git add -u (-u because we need to account for deleted files as well.)
    git status (to see if all files are marked as added).
    git commit --amend
    git log (To see if your commit changed).

4. Run "git checkout -b mergeme origin/master" to create a new repository from remote master.

5. Run "git merge somethingsome" to merge 
