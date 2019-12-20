# Git CDD
Git plugin for Commit Driven Development

## NAME
git-cdd – git plugin for commit driven development

## SYNOPSIS
```
git cdd <command> [options] [arguments]
```

## DESCRIPTION
Git CDD is a git plugin (i.e. it wont work without git).

The purpose of CDD is to:

* make you focused on the task ahead without your mind wandering off
* keep your work within your current scope
* improve readability and traceability of your commits (for your future-you and others)

You create a commit message before changing any files. Any changes to be committed later on
should stay within the previously defined scope.

## INSTALLATION
Clone this repository:
```
git clone git@github.com:alpipego/git-cdd.git
```

Install using make, the files will be move to `/usr/local/bin`
```
sudo make install
```

Uninstall the same way `sudo make uninstall`.

## FILES
/usr/local/bin/cdd-shared  
/usr/local/bin/git-cdd  
/usr/local/bin/git-cdd-aim  
/usr/local/bin/git-cdd-amend  
/usr/local/bin/git-cdd-fire  
/usr/local/bin/git-cdd-forget  
/usr/local/bin/git-cdd-status  

## COMMANDS

### aim
`git cdd aim` – Setup a commit message.

Options:

* `-m, --message <message>`  
commit message

If no message gets passed, this will open your editor of choice.

### amend
`git cdd amend` – Update the commit message to reflect changes in scope.

### fire
`git cdd fire` – Commit your changes.

This passes all options through to git commit, except:  
  `-F, --file <file>`  
  `-m, --message <message>`  
  `-c, --reedit-message <commit>`  
  `-C, --reuse-message <commit>`  
  
Check git commit -h for more information.

### forget
`git cdd forget` – Remove commit message.

Options:

* `--force`  
  also remove tracked and uncommitted changes
* `--clean`  
  also remove untracked files and directories

### status
`git cdd status` – Get the CDD status.
  
This passes all options through to git status.

Check git status -h for more information.

## Further Reading

* https://hofmannsven.com/2019/commit-message-driven-development
