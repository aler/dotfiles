# How to install

	mkdir ~/repos
	cd ~/repos
	git clone git://github.com/aler/dotfiles.git
	cd
	
	#links
	ln -nfs repos/dotfiles/bash/bashrc .bashrc
	ln -nfs repos/dotfiles/bash/bash_profile .bash_profile

	#vcprompt
	#you might need sudo get-apt install build-essential on Ubuntu
	cd /tmp
	wget http://vc.gerg.ca/hg/vcprompt/archive/tip.tar.gz
	mkdir vcprompt
	tar xvzf tip.tar.gz -C vcprompt
	cd vcprompt
	make
	cp vcprompt ~/bin

	cd
	source ~/.bashrc

