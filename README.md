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

## How to do it

1. Make sure your on the branch that will recieve the commit you're replicating
2. Find the commit hash of the commit you want to copy
3. Run `git cherry-pick REPLACE-ME-WITH-COMMIT-ID-YOUR-COPYING`
4. Deal with the results, this could work, result in a merge confilct you'd need to resolve, or report that the cherry pick would result in an empty commit in which case you can choose to skip or allow the empty commit

## Practice

We'll try to take three commits from the main branch to the target branch. The
first will apply cleanly. The second will result in a merge conflict and the
third will error as the changes will already exist in the new code.

Switch to the target branch
    ```git switch target```

Try to cherry pick the following commits from the main branch to the target branch

1. add gitignore
2. fix exercise instructions
3. add example.md
