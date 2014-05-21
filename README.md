GoalCoin Technical Specifications
========================

 - Srypt proof-of-work algorithm
 - 60 second block time target
 - ~2.3 million coins, 0.03 block reward after that
 - 2 coins per block, reducing 1% every ~1 week
 - Retarget every minute
 
Ubuntu Dependencies
===================
sudo apt-get install build-essential libboost-all-dev libcurl4-openssl-dev libdb5.1-dev libdb5.1++-dev git qt-sdk libminiupnpc-dev

sudo apt-get install qrencode libqrencode-dev 

Ubuntu Compile goalcoind
========================
cd ~

git clone git://github.com/goalcoin/goalcoinwallet.git

cd /goalcoinwallet/src

make -f makefile.unix USE_UPNP=-

sudo cp goalcoind /usr/bin


When trying to compile if you get this error: "../share/genbuild.sh: 34: ../share/genbuild.sh: cannot create obj/build.h: Directory nonexistent
make: *** [obj/build.h] Error "

Make sure to create the folder "obj" in the "src" folder:

cd /goalcoinwallet/src

If Root: cd ~/goalcoinwallet/src

mkdir obj

Then try compiling again.


Ubuntu Compile goalcoin-qt
========================
cd GoalCoinProject

qmake "USE_UPNP=-" goalcoin-qt.pro

make

Links
======

Website: http://www.goalco.in

Twitter: https://twitter.com/goalcoin




