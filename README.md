## OSX
```
brew install qt5
brew link --force qt5
ln -s /usr/local/Cellar/qt/5.11.0/mkspecs /usr/local/mkspecs
ln -s /usr/local/Cellar/qt/5.11.0/plugins /usr/local/plugins
ln -s ../bbscoin/ cryptonote
mkdir build && cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
make
```

## Ubuntu
```
sudo apt-get install build-essential libboost-all-dev git cmake qtbase5-dev
git clone https://github.com/bbscoin/bbscoin.git
cd ..
git clone https://github.com/bbscoin/bbscoin-wallet.git
cd bbscoin-wallet
ln -s ../bbscoin/ cryptonote
mkdir build && cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
make
```


## centos 7
```
yum install build-essential libboost-all-dev git cmake3 qt5-qtbase-devel boost boost-devel  -y 

yum install git cmake gcc-c++ gcc glibc-static wget libstdc++-static -y
wget https://dl.bintray.com/boostorg/release/1.66.0/source/boost_1_66_0.tar.gz
tar xzvf https://dl.bintray.com/boostorg/release/1.66.0/source/boost_1_66_0.tar.gz
cd boost_1_66_0
./bootstrap.sh
./b2 install
cd ..


git clone https://github.com/bbscoin/bbscoin.git
git clone https://github.com/bbscoin/bbscoin-wallet.git
cd bbscoin-wallet
ln -s ../bbscoin/ cryptonote
mkdir build && cd build
cmake3 .. -DCMAKE_BUILD_TYPE=Release
cd ..
make
```

## Windows

Clone the bbscoin first,

```
git clone https://github.com/bbscoin/bbscoin.git bbscoin
```

Now, you should compile the BBSCoin dynamic libs first.
Then copy these files to the libs dir.

Finally, use CMake and VS compile this project.

## Windows Pre-built

Following dependencies need to be installed before running the wallet:

Windows binary require VC2017 runtime.
Download from https://aka.ms/vs/15/release/vc_redist.x64.exe

Universal C Runtime
https://support.microsoft.com/en-us/help/2999226/update-for-universal-c-runtime-in-windows
