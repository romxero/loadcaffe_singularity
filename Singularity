Bootstrap: docker
From: ubuntu:16.04

%labels
Author "Randall Cab White - rcwhite@stanford.edu"

#########
#%setup
#########

##Just grabbing default packages from ubuntu repository
%post
	apt-get -ym update
	apt-get -ym install git libcgal-dev
    apt-get -ym install bison cmake flex gcc g++ # GNU toolchain
    apt-get -ym install gsl-bin libgsl-dev # GSL
    apt-get -ym install luarocks 
    
    
    wget https://luarocks.org/releases/luarocks-3.0.4.tar.gz
	tar zxpf luarocks-3.0.4.tar.gz
	cd luarocks-3.0.4
	./configure; sudo make bootstrap
	sudo luarocks install luasocket
	lua

%environment
	export IMAGE_NAME="NCO"

