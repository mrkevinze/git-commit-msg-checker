# Git Commit Message Checker

Checks that git commit messages are formatted according to certain guidelines documented in `guidelines.txt`.

## Installation

1. Give the `commit-msg` file permissions to execute, e.g. `chmod u+x commit-msg`
2. Copy the `commit-msg` file into the `.git/hooks` folder of your git repository.
3. The script will be executed by git locally when a git commit is performed.

The script is also known as a git hook.

## Discussion

The advantage to running the script locally is that it is simple and errors can be caught before a commit is done. The downside is that the user may forget to install or update the script, or bypass it altogether.

The alternative is to install a server-side hook, so that the script runs when a push is done. If the check fails, the push will be rejected. To do this, rename the script to use an appropriate hook. Remember to handle different arguments specific to each different hook.

## References
[Git Hooks](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks)  
[Tutorial by Atlassian](https://www.atlassian.com/git/tutorials/git-hooks/local-hooks)
