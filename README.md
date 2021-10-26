# vv-docker

## 0. git clone
```
git clone https://github.com/jingu-lee/vv-docker.git
cd vv-docker
```

## 1. nvidia driver setup
```
bash nvidia_install.sh
```

## 2. docker setup
```
bash docker_install.sh
```

## 3. cuda setup
```
sudo update
wget https://developer.download.nvidia.com/compute/cuda/11.3.1/local_installers/cuda_11.3.1_465.19.01_linux.run
sudo sh cuda_11.3.1_465.19.01_linux.run --silent --toolkit
sudo sh -c "echo 'export PATH=$PATH:/usr/local/cuda-11.3/bin' >> /etc/profile"
sudo sh -c "echo 'export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/cuda-11.3/lib64' >> /etc/profile"
sudo sh -c "echo 'export CUDADIR=/usr/local/cuda-11.3' >> /etc/profile"
source /etc/profile
echo "CUDA TOOLKIT INSTALL AND PATH SETTING DONE"
sudo reboot
```
