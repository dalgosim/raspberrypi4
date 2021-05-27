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
sudo apt-get install rustc cargo
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
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
