Latinio LTN development tree

Latinio is a PoS-based cryptocurrency.

Development process
Developers work in their own trees, then submit pull requests when they think their feature or bug fix is ready.

The patch will be accepted if there is broad consensus that it is a good thing. Developers should expect to rework and resubmit patches if they don't match the project's coding conventions (see coding.txt) or are controversial.

The master branch is regularly built and tested, but is not guaranteed to be completely stable. Tags are regularly created to indicate new stable release versions of Latinio.

Feature branches are created when there are major new features being worked on by several people.

From time to time a pull request will become outdated. If this occurs, and the pull is no longer automatically mergeable; a comment on the pull will be used to issue a warning of closure. The pull will be closed 15 days after the warning if action is not taken by the author. Pull requests closed in this manner will have their corresponding issue labeled 'stagnant'.

Issues with no commits will be given a similar warning, and closed after 15 days from their last activity. Issues closed in this manner will be labeled 'stale'.

=========================================== Install
Linux Ubuntu 18.04
------------------
Library:
--------
    sudo apt-get -y install software-properties-common nano build-essential qt5-default qt5-qmake qtbase5-dev-tools qttools5-dev-tools  libdb++-dev libboost-all-dev libminiupnpc-dev automake autoconf git pkg-config libjansson-dev libgmp-dev make g++ gcc libqrencode-dev qrencode libminiupnpc-dev automake autoconf 

    sudo apt-get -y install  libcurl-openssl1.0-dev libssl1.0-dev libcurl3

    sudo env LC_ALL=C.UTF-8 add-apt-repository -y ppa:bitcoin/bitcoin
    sudo apt-get -y update
    sudo apt-get -y install libdb4.8-dev libdb4.8++-dev
    
    git clone https://github.com/blockchaintechnologysas/latinio.git
    
    cd Latinio/src
    make -j$(nproc) -f makefile.unix

    strip latiniod
    chmod +x latiniod
    mv latiniod /usr/bin/

    mkdir ~/.latinio
    nano ~/.latinio/latinio.conf
    
Paste the following lines in latinio.conf:

    rpcuser=rpc_latinio
    rpcpassword=69c863e3356d3dae95df454a1
    rpcallowip=127.0.0.1
    listen=1
    server=1
    txindex=1
    daemon=1
    addnode=178.18.254.7
    addnode=161.97.105.211
    addnode=161.97.105.215
    addnode=161.97.107.21
    addnode=161.97.107.33
    addnode=161.97.115.236
    addnode=161.97.118.136
    addnode=161.97.118.137
    addnode=161.97.73.111
    addnode=161.97.74.7
    addnode=161.97.75.141
    addnode=161.97.77.29
    addnode=167.86.100.17
    addnode=167.86.121.176
    addnode=167.86.78.188
    addnode=167.86.82.30
    addnode=173.212.247.187
    addnode=178.18.254.7
    addnode=178.238.237.90
    addnode=179.32.81.106
    addnode=190.61.47.117
    addnode=193.37.152.88
    addnode=50.220.121.211
    addnode=62.171.147.226
    addnode=62.171.156.62
    addnode=62.171.184.178
    addnode=91.205.173.27
    addnode=95.111.234.144
    
Ctrl + x Y (Yes) (Enter)

start:

     latiniod
     
Stop:

    latiniod stop

Info:

    latiniod getinfo
    
New Address:

    latiniod getnewaddress
    
Help:

    latiniod help
