git-helpers
===========

A fork of codenga-helpers

# Installing it

    git clone git://github.com/pahko/git-helpers.git
    cd git-helpers
    git_helpers_path=$(pwd)
    cat >> ~/.bashrc <<EOF
    # Codenga-helpers
    source ${git_helpers_path}/git-helpers
    EOF
    
add this to your `.bashrc` at the end of file to enable branch name on prompt

    PS1='\[\e[1;32m\][\u@\h\w\[\e[1;34m\]$(git_branch_p)\[\e[0m\]\[\e[1;32m\]]\[\e[0m\]\n\[\e[1;36m\]\$\[\e[0m\] '