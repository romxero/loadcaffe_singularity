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
    
    

	luarocks install luasocket
	

%environment
	export IMAGE_NAME="NCO"

