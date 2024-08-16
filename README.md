# Cherry Pick Kata

A git repo for practicing cherry picking commits.

## What is a cherry pick?

According to GitLab, cherry-picking is taking a single commit from one branch and adding it
as the latest commit on another branch. The rest of the commits in the source branch
are not added to the target.

Cherry-pick a commit when you need the contents in a single commit, but not the
contents of the entire branch. For example, when you:

* Backport bug fixes from the default branch to previous release branches.
* Copy changes from a fork to the upstream repository.

[Source](https://docs.gitlab.com/ee/user/project/merge_requests/cherry_pick_changes.html)
Also see [https://www.git-scm.com/docs/git-cherry-pick]

## Practice

We'll try to take three commits from the main branch to the target branch. The
first will apply cleanly. The second will result in a merge conflict and the
third will error as the changes will already exist in the new code.

Switch to the target branch
    ```git switch target```

1. Try to cherry pick the 'add git log commit'
2. Try to cherry pick the 'add git log commit'
3. Try to cherry pick the 'add git log commit'
