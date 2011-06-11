How to install
==============

mkdir ~/repos
cd ~/repos
git clone git://github.com/aler/dotfiles.git
cd

ln -nfs repos/dotfiles/bash/bashrc .bashrc
ln -nfs repos/dotfiles/bash/bash_profile .bash_profile
ln -nfs repos/dotfiles/vim/vimrc .vimrc
ln -nfs repos/dotfiles/vim/gvimrc .gvimrc
ln -nfs repos/dotfiles/vim .vim
ln -nfs repos/dotfiles/gitconfig .gitconfig

brew install ack
cd repos/dotfiles
git submodule init
git submodule update
cd vim/bundle/command-t
rake make
cd

cd /tmp
wget http://vc.gerg.ca/hg/vcprompt/archive/tip.tar.gz
mkdir vcprompt
tar xvzf tip.tar.gz -C vcprompt
cd vcprompt
make
cp vcprompt ~/bin

cd
source ~/.bashrc

