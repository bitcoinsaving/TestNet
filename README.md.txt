BitcoinSaving Cryptocurrency Testnet 
------------------------------------

This is use for bitcoinsaving testnet propose only.

It's a full copy of mainnet source code except:
The Genesis hash Block, MapCheckpoints, Internet port, Premine (mainnet is set to 1% premine).

Testnet Wallet can be download here: https://github.com/bitcoinsaving/TestNet/tree/master/Wallet


Install for Linux Daemon
------------------------

* Install dependencies listed below.

wget https://github.com/bitcoinsaving/TestNet/blob/master/Wallet/testnet-daemon-linux.tar.gz  //Compile on Ubuntu 14.04
or
wget https://github.com/bitcoinsaving/TestNet/blob/master/Wallet/testnet-daemon-ubuntu1604.tar.gz //Compile on Ubuntu 16.04

tar -xzvf testnet-daemon-linux.tar.gz     //or testnet-daemon-ubuntu1604.tar.gz

chmod +x bitcoinsavingd

run it with: ./bitcoinsavingd    or   ./testnet

* After the first run you will get the following massage, please follow the instruction:
Error: To use bitcoinsavingd, you must set a rpcpassword in the configuration file:
/root/.bitcoinsaving/bitcoinsaving.conf
It is recommended you use the following random password:
rpcuser=<auto-generate user>
rpcpassword=<auto-generate password>
(you do not need to remember this password)

For security reasons the username and password MUST NOT be the same.

Run it again.


Install for Windows 7/8/10
--------------------------

download & unzip & run: https://github.com/bitcoinsaving/TestNet/blob/master/Wallet/bitcoinsaving-qt-windows.zip 


Install for Linux Xwindows
--------------------------

wget 
https://github.com/bitcoinsaving/TestNet/blob/master/Wallet/bitcoinsaving-qt-linux.tar.gz

tar -xzvf bitcoinsaving-qt-linux.tar.gz

* Run it inside Xwindows.


Linux dependencies for Ubuntu 16.04
-----------------------------------

sudo apt-get update
sudo apt-get upgrade

sudo apt-get install build-essential libssl-dev libdb-dev libdb++-dev libboost-all-dev git libssl1.0.0-dbg -y

sudo apt-get install libdb-dev libdb++-dev libboost-all-dev libminiupnpc-dev libminiupnpc-dev libevent-dev libcrypto++-dev libgmp3-dev -y


Linux dependencies for Ubuntu 14.04
-----------------------------------

sudo apt-get update
sudo apt-get upgrade

sudo apt-get install build-essential libssl-dev libdb-dev libdb++-dev libboost-all-dev git libssl1.0.0-dbg -y

sudo apt-get install libdb-dev libdb++-dev libboost-all-dev libminiupnpc-dev libminiupnpc-dev libevent-dev libcrypto++-dev libgmp3-dev -y

sudo apt-get install libboost1.54-all-dev libdb-dev libdb++-dev install libminiupnpc-dev -y


Install linux daemon from source
--------------------------------

sudo apt-get install libboost-all-dev g++-5 libssl-dev libdb++-dev -y 
sudo apt-get install build-essential libssl-dev libdb-dev libdb++-dev libboost-all-dev git libssl1.0.0-dbg -y
sudo apt-get install libdb-dev libdb++-dev libboost-all-dev libminiupnpc-dev libminiupnpc-dev libevent-dev libcrypto++-dev libgmp3-dev -y
mkdir testnet
cd testnet
wget https://github.com/bitcoinsaving/TestNet/blob/master/Wallet/bitcoinsaving-source.tar.gz
tar -xzvf bitcoinsaving-source.tar.gz
cd src
make -f makefile.unix RELEASE=1


How to Mine a block
-------------------

Open your wallet on windows.

Close your wallet and create the file bitcoinsaving.conf in the folder "%APPDATA%\bitcoinsaving\".

Copy the following text into BitcoinSaving.conf and save the file:

rpcuser=<auto-generate user>
rpcpassword=<auto-generate password>
rpcallowip=127.0.0.1
rpcport=35280
listen=1
server=1
addnode=testnet1.bitcoinsaving.cc
addnode=testnet2.bitcoinsaving.cc
addnode=testnet3.bitcoinsaving.cc
addnode=testnet4.bitcoinsaving.cc

Download cpuminer from https://bitcointalk.org/index.php?topic=55038.0 and extract the zip file.

Create a .bat file named mine.bat and copy the following text into mine.bat.

minerd --url=http://127.0.0.1:35280 --userpass=rpc_user:<auto-generate password that been configured at bitcoinsaving.conf file>

Save the file inside the extracted cpuminer folder.

Open your wallet and execute mine.bat to start mining.


Testnet Explorer & API
----------------------

Testnet Explorer located at http://testnet.bitcoinsaving.cc
Testnet API Documentation located at http://testnet.bitcoinsaving.cc/info



