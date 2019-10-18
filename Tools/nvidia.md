# install nvidia-driver

# install nvidia-cuda

download **CUDA 10.1** from here [http://developer.download.nvidia.com/compute/cuda/10.1/Prod/local_installers/cuda_10.1.243_418.87.00_linux.run]()

    ~$ sudo sh cuda_10.1.243_418.87.00_linux.run
        "if you have installde a driver, do not select driver when cuda installing"

configure environment path

    ~$ export CUDA_HOME=/usr/local/cuda 
    ~$ export PATH=$PATH:$CUDA_HOME/bin 
    ~$ export LD_LIBRARY_PATH=/usr/local/cuda-10.0/lib64${LD_LIBRARY_PATH+:${LD_LIBRARY_PATH}}
    ~$ source ~/.bashrc

running a test

    ~$ cd /usr/local/cuda/samples/1_Utilities/deviceQuery 
    ~$ sudo make
    ~$ ./deviceQuery
        "if you get pass"
