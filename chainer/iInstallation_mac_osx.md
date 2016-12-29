# Installation Mac OSX
## Install Python
```
$ brew update
$ brew install python
$ pip install --upgrade pip setuptools
$ brew linkapps python
$ vim ~/.bash_profile
export PATH=/usr/local/bin:/usr/local/share/python:$PATH
$ source ~/.bash_profile
$ which python
/usr/local/bin/python
```

## Install dependent libraries
```
$ sudo pip install numpy

# $ sudo easy_install --upgrade numpy
# $ sudo easy_install --upgrade six

$ sudo pip install protobuf
$ sudo pip install pillow
$ sudo pip install h5py
$ sudo pip install cython
$ brew tap homebrew/science
$ brew install hdf5
$ sudo pip install chainer
```
ref - http://walkingmask.hatenablog.com/entry/2015/11/16/224638
