## pytorch
### install related packages
```
sudo apt install libopenblas-dev libblas-dev m4 cmake cython python3-dev python3-yaml python3-setuptools
sudo apt-get install libavutil-dev libavcodec-dev libavformat-dev libswscale-dev
```

### install pytorch whl
https://github.com/sungjuGit/PyTorch-and-Vision-for-Raspberry-Pi-4B
* 혹시몰라 fork 해둠. 없어지면 개인 repo에서 찾을 것
```
python3 -m pip install torch-1.8.0a0+56b43f4-cp37-cp37m-linux_armv7l.whl
python3 -m pip install torchvision-0.9.0a0+8fb5838-cp37-cp37m-linux_armv7l.whl
```
## tensorflow
### install related packages
```
sudo apt install libatlas-base-dev
```

### install tensorflow
```
pip3 install tensorflow
```

## sentencepiece
### install related packages
```
sudo apt-get install cmake build-essential pkg-config libgoogle-perftools-dev
sudo apt-get install autoconf automake libtool libprotobuf-c++ protobuf-compiler libprotobuf-dev
sudo apt-get install rustc cargo
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

sudo apt-get install libatomic-ops-dev
```


### build sentencepiece
```
git clone https://github.com/google/sentencepiece.git 
cd sentencepiece
mkdir build
cd build
cmake ..
make -j $(nproc)
sudo make install
sudo ldconfig -v
```

#### build 할 때, 오류나는 부분에 옵션 추가
```
# 오류 샘플
# Building CXX object src/CMakeFiles/spm_normalize.dir/spm_normalize_main.cc.o

# 해당 경로의 link.txt 마지막에 -latomic 추가
>>> ~~~ libsentencepiece_train.so.0.0.0 libsentencepiece.so.0.0.0 -lpthread -ltcmalloc_minimal -latomic

# vi src/CMakeFiles/spm_train.dir/link.txt
# src/CMakeFiles/spm_decode.dir/link.txt
# src/CMakeFiles/spm_encode.dir/link.txt
```

### 
```
git clone https://github.com/Microsoft/vcpkg.git
cd vcpkg
./bootstrap-vcpkg.sh
./vcpkg integrate install
./vcpkg install sentencepiece
```
