You can setup a node using Ubuntu 14.04 server using the following instructions. 

Rent a VPS running Ubuntu 14.04 - PREF: Digital Ocean - https://m.do.co/c/4f1ff7b192ef

 
Update your VPS using the following commands. 

sudo apt-get update 
sudo apt-get upgrade 

Install the necessary dependencies using the following commands. 

sudo apt-get install build-essential libssl-dev libdb-dev libdb++-dev libboost-all-dev git libssl1.0.0-dbg 

sudo apt-get install libdb-dev libdb++-dev libboost-all-dev libminiupnpc-dev libminiupnpc-dev libevent-dev libcrypto++-dev libgmp3-dev

/src/leveldb Directory - Make sure to sudo chmod +x build_detect_platform before compiling

/src Directory - Compile the Source: make -f makefile.unix RELEASE=1

Attempt to start the daemon using ./litecoinblackd - it will echo stating a config file needs to be created. 

Create a config file. - Remaing in the /src directory

Type nano ~/.litecoinblack/litecoinblack.conf 

Paste the following lines in litecoinblack.conf - change the rpcusername & rpcpassword. 

daemon=1 

listen=1 

server=1 

rpcuser=RANDOM_USERNAME 

rpcpassword=RANDOM_LONG_PASSWORD 

rpcallowip=127.0.0.1 

rpcport=37546 

addnode=165.227.63.114

addnode=174.54.60.200

addnode=128.199.90.69 

addnode=5.100.139.61

addnode=104.231.101.169

addnode=149.56.6.7

addnode=69.21.70.44

addnode=174.31.131.56

addnode=213.127.58.47

addnode=45.56.149.107

addnode=5.189.177.212

addnode=167.99.190.52

addnode=116.96.165.93

addnode=14.231.28.193

addnode=176.107.204.136

addnode=70.68.168.243

addnode=210.211.124.189

addnode=165.227.63.114


Start the daemon again with the following command:

./litecoinblackd 

Your node is now online - to check the status type: ./litecoinblackd getinfo 

Lastly, message a developer or moderator on discord with your server's IP / Domain to have your node added to the list.
