Bootstrap: docker
From: debian:buster

IncludeCmd: yes

%labels
    AUTHOR icaoberg
    EMAIL icaoberg@alumni.cmu.edu
    WEBSITE http://linus.cbd.cs.cmu.edu
    VERSION 2.29.2

%post
    apt-get update
    apt-get install -y --no-install-recommends apt-utils software-properties-common
    apt-get update --fix-missing
    apt-get install -y openjdk-11-jdk
    apt-get install -y libfuse-dev fuse curl wget

####################################################################################
%appinstall score
    wget -O score-client.tar.gz https://artifacts.oicr.on.ca/artifactory/dcc-release/bio/overture/score-client/3.0.1/score-client-3.0.1-dist.tar.gz
    tar -xvzf score-client.tar.gz
    cd score-client-3.0.1  # or newer version
    mv -v bin/score-client /bin/

%apphelp score
    score-client --help    

%apprun score
    score-client "$@"
