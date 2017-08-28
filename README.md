# machine_setup
Contains files, such as vimrc and bashrc, for new machine setup.  Includes vim plugins i use

# Vim

For youcompleteme, it needs vim with python installed.

* echo has('python') must equal "1"
* py print('py3') will show what library it's trying to load up

On Windows Git Bash
* Note none of the vim installations on Git Bash really support python.  I've found doing this is sufficient for getting a python-enabled vim:
** Download vim from https://tuxproject.de/projects/vim/
** Make sure the directory containing "gvim" is in PATH, but _after_ the /usr/bin that GitBash uses
*** This means command-line vim will be old vim, but gvim will be fully enabled vim
** Create a symlink from vimfiles to the ~/.vim:
MAKE SURE TO DO THIS IN CMD AND NOT GIT BASH ON WINDOWS

cd C:\Users\<username>
mkline vimfiles .vim


Now gvim will use same autoload dir as command-line vim

For YouCompleteMe for Python:
* Do this in the ~/vimfiles/plugged/YouCompleteMe dir:
git submodule update --init --recursive
In order to get thirdparty dir
