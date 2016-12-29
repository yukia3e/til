# Installing cuda & cudnn (osx)
2016/12/29

## cuda
```shell-session
$ brew update
$ brew cask info cuda
cuda: 7.5.20
$ brew cask install cuda
$ vim ~/.bash_profile
export CUDA_ROOT=/usr/local/cuda
export PATH=$CUDA_ROOT/bin:$PATH
export DYLD_LIBRARY_PATH=$CUDA_ROOT/lib:$PATH
$ cd /Developer/NVIDIA/CUDA-8.0/samples
$ sudo make -C 1_Utilities/deviceQuery
$ cd bin/x86_64/darwin/release/
$ ./deviceQuery
```

## cudnn
- Download cuDNN Library for osx  
-- [link](https://developer.nvidia.com/rdp/cudnn-download)

- copy files
```
$ tar xzvf ~/Downloads/cudnn-8.0-osx-x64-v5.1.tgz
$ sudo mv -v cuda/lib/libcudnn* /usr/local/cuda/lib
$ sudo mv -v cuda/include/cudnn.h /usr/local/cuda/include
```
