#! /bin/bash

check() {
    if pacman -Qi $1 > /dev/null ; then
        echo "System has $1"
    else
        pacman -S $1 --noconfirm
    fi
}

check git
check httpie

git clone ssh://git@github.com/TomiEckert/dotfiles

cd dotfiles

echo "type 'sudo sh install.sh' or check out the install.sh to see that it won't bite ya dick off"
