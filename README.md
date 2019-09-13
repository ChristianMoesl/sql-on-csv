```
git clone https://github.com/WebAssembly/wabt
cd wabt
docker run -it -v $(pwd):/opt/wabt
yum groupinstall "Development Tools"
yum install wget file clang
wget https://cmake.org/files/v3.10/cmake-3.10.0.tar.gz
tar -xvzf cmake-3.10.0.tar.gz
cd cmake-3.10.0
export CC=gcc
export CXX=g++
yum remove cmake
./bootstrap
make
make install
ln -s /usr/local/bin/cmake /usr/bin/cmake
make clang-release-no-tests
```

/opt/wabt/out/clang/Release/no-tests/wat2wasm