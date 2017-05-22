Caffe `Makefile.config`
=======================

Caffe has lots of options and any small mistake can lead you off track for
hours. I've successfully compiled and run [Caffe] for my own **Macbook Pro
(Retina, Mid 2012)** under following conditions:


`Makefile.config.os.x`
----------------------

* macOS Sierra 10.12.4
* NVIDIA&reg; CUDA&trade; 8.0.83 with cudnn
* Xcode CLT(Command Line Tools) 8.2 (Apple clang 80000)
* OpenCV 3.2.0
* Python 3.6
* numpy 1.12.1
* ATLAS BLAS
* boost 1.64.0

[Caffe]: http://caffe.berkeleyvision.org


Notes
-----

Sometimes CUDA is not supported with the latest version of the Apple LLVM and
output an error message as follows.

`nvcc fatal : The version ('80100') of the host compiler ('Apple clang') is not supported`

The current CUDA driver 8.0.83 supports Xcode CLT 8.2 so you should switch to
the old version.

1. Log in to https://developer.apple.com/downloads/
2. Download Xcode CLT (Command Line Tools) 8.2
3. Install CLT
4. Run `sudo xcode-select --switch /Library/Developer/CommandLineTools`
5. Verify that clang has been downgraded via clang --version
