## OSX
```
brew install qt5
mkdir build && cd build
cmake .. -DCMAKE_BUILD_TYPE=Release -DCMAKE_PREFIX_PATH=/usr/local/Cellar/qt/5.10.0_1
make
```

## Ubuntu
```
git clone https://github.com/altcnews/Nirvana-Wallet.git
cd Nirvana-Wallet
ln -s ../Nirvana/ cryptonote
mkdir build && cd build
cmake ..
make
```

## Windows

Clone the Nirvana first,

```
git clone https://github.com/altcnews/Nirvana.git
```

Now, you should compile the Nirvana dynamic libs without rocksdb first, comment "add_subdirectory(tests)" line in Nirvana/CMakeLists.txt, and compile the packages/rocksdb-rocksdb-4.11.2.zip dynamic libs.
Then copy these files to the libs dir.

Finally, use CMake and VS compile this project.

## Windows Pre-built

Following dependencies need to be installed before running the wallet:

Windows binary require VC2017 runtime.
Download from https://aka.ms/vs/15/release/vc_redist.x64.exe

Universal C Runtime
https://support.microsoft.com/en-us/help/2999226/update-for-universal-c-runtime-in-windows
