Localhooks for scip
----------

These git hooks help to check the correct format of commits before pushing.
They need to be installed by the user for the local repository.
For instructions please continue reading.

Available hooks:
----------------

 - commit-msg: checks every commit message for correct format (line length, etc.)
 - pre-commit: checks every commit for trailing whitespaces, filename format and that the files size does not exceed 50 MB

Instructions for local hooks
-----------------

Hooks are scripts that run before or after certain events
in Git. The `commit-msg` hook for example runs after the
commit message is edited and checks for the correct format.

For security reasons, local hooks have to be activated
manually for every single repository.

There are several ways of doing that:

1. Run `installhooks` and follow the steps
   (this method will create links to the hooks just like method 2)

2. Create links from
   `.git/hooks/`
   in every repository to the scripts in this localhooks/ folder you like to use.
   example:
```
   cd scip/.git/hooks
   ln -s /path/to/localhooks/commit-msg
```
3. Copy the contained hooks into the directory
   `.git/hooks/`
   of your local repository.
