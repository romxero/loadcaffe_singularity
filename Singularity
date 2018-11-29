Bootstrap: docker
From: ubuntu:18.04

%labels
Author "Randall Cab White - rcwhite@stanford.edu"

#########
#%setup
#########

##Just grabbing default packages from ubuntu repository
%post
	apt-get -ym update
    apt-get -ym install git bison cmake flex gcc g++ tcl-tclreadline # GNU toolchain
    apt-get -ym install libprotobuf-dev protobuf-compiler # GSL
    apt-get -ym install readline-common libreadline-dev #readline
    apt-get -ym install openssl libssl-dev  
    apt-get -ym install wget curl zip #grabbing utilities
	
	mkdir -p /home
	cd /home
	git clone https://github.com/torch/distro.git ~/torch --recursive
	cd ~/torch
	./clean.sh
	./install.sh
	ls -lrths 
	
#	luarocks install image
#	luarocks list
	
	
	#luarocks install luasocket
	#luarocks install luasec
	#luarocks install loadcaffe
	

%environment
	export IMAGE_NAME="LOAD_CAFFE"

