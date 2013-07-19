[user]
        name = Jørgen Jacobsen
        email = **************
[alias]
        br = branch
        bra = branch -a
        brr = branch -r
        ci = commit
        civ = commit -v
        co = checkout
        di = diff
        st = status
        rb = rebase
        com = !git add . && git add -u && git commit
        unstash = stash pop
        slog = log --pretty=format:'%h %ar by %an: %s'
        toplist = !git-toplist
        new-project = !fronter-new-project
        new-empty-project = !fronter-new-empty-project
        new-branch = !fronter-new-branch
        review-create = !git-review-create
        review-update = !git-review-update
        get-merge-request = !sh -c '(git branch -D merge-requests/$1 2> /dev/null || echo -n "") && git fetch $(git config remote.upstream.url) refs/merge-requests/$1:merge-requests/$1' -
        show-details-merge-request = !sh -c 'git log -p --pretty=oneline --abbrev-commit $(git-current-branch)..merge-requests/$1' -
        show-merge-request = !sh -c 'git diff --pretty=oneline --abbrev-commit $(git-current-branch)..merge-requests/$1' -
        hist = log --pretty=format:\"%h %ad | %s%d [%an]\" --graph --date=short

[color]
        branch = auto
        diff = auto
        interactive = auto
        status = auto
        ui = auto
[color "branch"]
        current = bold
        remote = yellow
[core]
        editor = vim
        excludesfile = /Users/jorgenjacobsen/.gitignore_global
	quotepath = false
[merge]
        verbosity = 5