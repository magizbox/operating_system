# Ubuntu

### Apps

#### Install git

```shell
apt-get install -y git
```

### GUI `ubuntu-desktop

```
apt-get install ubuntu-desktop
```

Then restart computer, ubuntu-desktop will run in the next login.

# Install IntellIJ in ubuntu


###  Downloads intellij
```
https://www.jetbrains.com/idea/download/
```


### Create Ubuntu desktop launcher

run intellij : cd to folder intellij

```
cd file://path intellij/idea.sh
```

Create Ubuntu desktop

```
Tools > Create Desktop Entry
```

# Install Pycharm on Ubuntu

Step 1. To add the PPA, open terminal from the Dash, Launcher, or via Ctrl+Alt+T shortcut keys. When it opens, run command:

```
sudo add-apt-repository ppa:mystic-mirage/pycharm
```

Step 2. After adding the PPA, update system package cache and install the IDE via Synaptic Package Manager. Or just run below commands one by one in terminal:

```
sudo apt-get update

sudo apt-get install pycharm
```

Step 3. After finishing the installation, start Pycharm. It will prompt you to activate with license, choose the `License Server` checkbox and copy below row to it:

```
http://idea.qinxi1992.cn
```

# Install NVDIA Driver in Ubuntu 16.04


```
$ lspci | grep -i nvidia

sudo apt purge nvidia-*** nvidia-settings
sudo add-apt-repository ppa:graphics-drivers/ppa
sudo apt-add-repository ppa:xorg-edgers/ppa 
sudo apt update
sudo apt dist-upgrade
sudo apt install nvidia-381
sudo reboot
```

3. Verify GPU driver installation

```
$ nvidia-smi

Mon Oct  9 08:38:24 2017       
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 381.22                 Driver Version: 381.22                    |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|===============================+======================+======================|
|   0  GeForce GTX 980     Off  | 0000:01:00.0      On |                  N/A |
|  0%   44C    P8    16W / 196W |    527MiB /  4035MiB |      0%      Default |
+-------------------------------+----------------------+----------------------+
                                                                               
+-----------------------------------------------------------------------------+
| Processes:                                                       GPU Memory |
|  GPU       PID  Type  Process name                               Usage      |
|=============================================================================|
|    0      1106    G   /usr/lib/xorg/Xorg                             290MiB |
|    0      2340    G   compiz                                         147MiB |
|    0      5309    G   ...el-token=2868BBA605F5AD7A475E4323058D9F6C    86MiB |
+-----------------------------------------------------------------------------+
```

Install CUDA

1. Download `deb (local)` from https://developer.nvidia.com/cuda-80-ga2-download-archive

2. Run command

```
sudo dpkg -i cuda-repo-ubuntu1604-8-0-local-ga2_8.0.61-1_amd64.deb
sudo apt-get update
sudo apt-get install cuda
```

3. Configure PATH

Edit `~/.bashrc`

```
export PATH="/usr/local/cuda-8.0/bin:$PATH"
```

4. Verify CUDA Installation

```
$ nvcc --version

nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2016 NVIDIA Corporation
Built on Tue_Jan_10_13:22:03_CST_2017
Cuda compilation tools, release 8.0, V8.0.61
```

References:

* http://www.pradeepadiga.me/blog/2017/03/22/installing-cuda-toolkit-8-0-on-ubuntu-16-04/
* https://askubuntu.com/questions/799184/how-can-i-install-cuda-on-ubuntu-16-04
