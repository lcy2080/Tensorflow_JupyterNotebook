# Tensorflow_JupyterNotebook
Tensorflow with Jupyter Notebook Examples

This repository is for practicing Git, Github, Tensorflow, Jypyter Notebook and so on.

Environment : Windows 10
***
### Install CUDA

[Tensorflow-gpu 1.10.0 available version of CUDA, cuDNN Information Reference](https://github.com/yaroslavvb/tensorflow-community-wheels/issues/77)

[CUDA 9.2 Page](https://developer.nvidia.com/cuda-92-download-archive)<br>
[CUDA 9.2 Download](https://developer.nvidia.com/compute/cuda/9.2/Prod2/network_installers2/cuda_9.2.148_win10_network)

[cuDNN Archive](https://developer.nvidia.com/rdp/cudnn-archive)<br>
[cuDNN 7.2 for Windows10](https://developer.nvidia.com/compute/machine-learning/cudnn/secure/v7.2.1/prod/9.2_20180806/cudnn-9.2-windows10-x64-v7.2.1.38)

To access the cuDNN download page, you must subscribe to an NVIDIA membership.
###Install Anaconda

[Anaconda Downloads Page](https://www.anaconda.com/download/)<br>
Anaconda Download Link : [Anaconda 5.2 (Python 3.6, 64bit, Windows 10)](https://repo.anaconda.com/archive/Anaconda3-5.2.0-Windows-x86_64.exe)

### Install Tensorflow through Anaconda
- After install Anaconda Execute **Anaconda Prompt**

- Create new Anaconda Environment.<br>```>>conda create -n tensorflow python=3.6```

- Activate tensorflow env.<br>```>>activate tensorflow```
  - You can see the packages of activated env through next command.<br>```>>conda list```
  
- Update pip and install jupyter.<br>
```
>>python -m pip install --upgrade pip
>>conda install jupyter
```

- Before install tensorflow-gpu, install PyHamcrest first.<br>
```>>pip install PyHamcrest```

- Install tensorflow-gpu.<br>```>>pip install --ignore-installed --upgrade tensorflow-gpu```
  - If there is warning about setuptools version. type this command.<br>```conda install setuptools=39.1.0```
  
- Check jupyter path via below command.<br>```>>jupyter --path```
  - You can see the path **"ANACONDA_PATH\envs\tensorflow\share\jupyter"** on data path.
  - To add tensorflow env on jupyter notebook, duplicate **"python3"** folder on up path **"kernels"** folder. change **"kernel.json"** on up path "kernels" folder like below.
  ```
  {
  "argv": [
  "E:\\Anaconda\\envs\\tensorflow\\python.exe",
  "-m",
  "ipykernel_launcher",
  "-f",
  "{connection_file}"
  ],
  "display_name": "tensorflow",
  "language": "python"
  }
  ```
    - "E:\\Anaconda\\envs\\tensorflow\\python.exe" : you can see next command.<br>
      ```>>where python```
