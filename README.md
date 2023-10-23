# jetson_nano
steps for setting up jetson nano board.



## vscode installation

- https://code.visualstudio.com/docs/?dv=linuxarm64_deb

- sudo dpkg -i code_xxxxxxxxx_arm64.deb 

- sudo apt install apt-transport-https

- sudo apt update

## python dependencies

- sudo apt install python3-pip python-pip

- python3 -m pip install --upgrade pip

- pip3 install Pillow

- pip3 install segment-anything

- pip3 install opencv-python==4.7.0.68

- pip3 install pycocotools matplotlib onnxruntime onnx
  
- pip3 install torch torchvision

## stereo camera

- sudo apt install libcanberra-gtk-module libcanberra-gtk3-module -y

- https://github.com/ukhov79/Jetson-Nano-CSI-Stereo-Vision 

- If you find that the image captured is red. You can try to download .isp file and installed:

- wget https://files.waveshare.com/upload/e/eb/Camera_overrides.tar.gz

- tar zxvf Camera_overrides.tar.gz 

- sudo cp camera_overrides.isp /var/nvidia/nvcam/settings/

- sudo chmod 664 /var/nvidia/nvcam/settings/camera_overrides.isp

- sudo chown root:root /var/nvidia/nvcam/settings/camera_overrides.isp

## if touchpad does not work

- sudo apt remove fwupd

- sudo reboot


## to flash the SD card

- https://developer.nvidia.com/embedded/learn/get-started-jetson-nano-devkit

- if flashing fails: lock the SD card (https://github.com/balena-io/etcher/issues/3197 and https://www.minitool.com/data-recovery/sd-card-lock-unlock.html)

## viewing the pointcloud .ply in meshlab

- https://www.meshlab.net/#download
