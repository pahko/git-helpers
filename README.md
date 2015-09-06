git-helpers
===========

A set of git shortcuts and helpers to daily development.

# Installing it

    git clone git://github.com/pahko/git-helpers.git
    cd git-helpers
    git_helpers_path=$(pwd)
    cat >> ~/.bashrc <<EOF
    # Git Helpers
    source ${git_helpers_path}/git-helpers
    EOF

add this to your `.bashrc` at the end of file to enable branch name on prompt

    PS1='\[\e[1;32m\][\u@\h\w\[\e[1;34m\]$(git_branch_p)\[\e[0m\]\[\e[1;32m\]]\[\e[0m\]\n\[\e[1;36m\]\$\[\e[0m\] '

# Helpers usage

### add

Adds the specified paths for further commit. All changes in the current working directory are added in no paths specified.

    $ add file1 file2 path/to/file3 ../path/to/file_n  # adds these paths
    $ add  # same as [git add .]

### gcommit

A shortcut for `git commit -m <message>`

    $ gcommit <message>

### gdiff

A shortcut for `git diff`

### gpull

A shortcut for `git pull`.

#### gpush

Pushes all the locally changed branches to the `origin` repository.

### greset

Unstages the specified paths or the current working directory if no paths specified.

    $ greset file1 file2
    $ greset

### grm

A shortcut for `git rm` that retrieves the subsequent status after *removing* given path(s).

    $ grm <path1>[ path2[... path_n]]

### gundo

A shortcut to undo the latest commit and show the resulting status after undoing such commit.

### merge

A shortcut for `git merge`.

### newbranch

Creates and checks out to a new branch with the format specified for the project.

    $ newbranch <story number> <dash-separated description>
    Example:
    $ newbranch 100 short-description-here

### st

A shortcut for `git status`

### pull

Pulls changes only for the current branch

### push

Pushes only the current branch

### branches

List all branches, local and remote.
