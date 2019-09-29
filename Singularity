Bootstrap: docker
From: ubuntu:bionic

%labels
MAINTAINER Kokulapalan Wimalanathan
Version 1.1.0
Singularity Version 3.2.1

%environment
    export LC_ALL=C
    export DEBIAN_FRONTEND=noninteractive
    export MYSQL_USER=pannzer
    export MYSQL_DATABASE=pannzer
    export MYSQL_ROOT_PASSWORD=mysql

%files
    my.cnf 

%post
  export LC_ALL=C
  export DEBIAN_FRONTEND=noninteractive
  export TZ=America/Chicago
	echo "Running post.sh"
	apt-get -q -y update
	apt-get -yq install bsdutils lsb-base passwd perl psmisc debconf libc6 libevent-core-2.1-6 libgcc1 liblz4-1 libstdc++6 zlib1g gfortran rsync build-essential less vim wget python-pip libfuse2 r-base openjdk-8-jdk libidn11-dev libssl1.0-dev libssl1.0.0 git ncbi-blast+ octave octave-dataframe sqlite3 libsqlite3-dev python3-pip
	update-java-alternatives -s java-1.8.0-openjdk-amd64

	R -e 'install.packages(c("data.table","futile.logger","ontologyIndex","yaml"), repos="https://mirror.las.iastate.edu/CRAN/", Ncpus=16, INSTALL_opts="--no-html")'

	pip install numpy==1.14.5
	pip install scipy==1.1.0
	pip install jsonmerge==1.5.1
	pip install jsonschema==2.6.0
	pip install lxml==4.2.1
	pip install PyYAML==3.12
	pip install yamldirs==1.1.3
	pip install pyrocopy==0.8.0
	pip install requests==2.19.1
	pip install requests-toolbelt==0.8.0
	pip install numpydoc==0.8.0
	pip install biopython==1.70
	pip install joblib==0.12.2
	pip install natsort==5.3.3



	echo "=============================================="
	echo "Completed Post" 
	echo "=============================================="
