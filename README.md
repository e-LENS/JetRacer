# JetRacer

### Requirements

* Jetson Nano 2GB Developer Kit
  *  GPU : 128-core NVIDIA Maxwell architecture GPU
  *  CPU : Quad-core ARM® Cortex®-A57 MPCore processor
* Jetracer
  * Cam : Sony IMX219 Sensor, Resolution : 3280 x 2464  
* micro SD card (64GB~)
* balenaEtcher

### Installation

1. Format micro SD card before using.
2. Jetson Nano Image
* Download [jetson-nano-2gb-sd-card-image](https://developer.nvidia.com/jetson-nano-2gb-sd-card-image) & Uncompress 
* Write *Jetson Nano Image* in micro SD card using Etcher program.
* Put SD card into Jetson nano's SD card slot, and connect to the monitor using HDMI port. Finish system configuration
3. JetRacer Image
* Download [JetRacer image](https://drive.google.com/file/d/1YtnjQ77w1B9REzy1JgLJbVSs2K3ocAEr/view?usp=sharing) & Uncompress 
* Write *JetRacer Image* in micro SD card using Etcher program.
* Put SD card into Jetson nano's SD card slot, and connect to the monitor using HDMI port. Finish system configuration

(+)
* To activate GUI, use `sudo systemctl set-default graphical.target` command

### Connect to JetRacer

1. Connect JetRacer to WIFI network
2. Check ip address of Wlan0 interface using Jetson Nano's piOLED or `ifconfig` command
3. Connect to JetRacer wirelessly `http://<ip address>:8888`
4. Initial password is `jetbot`. Run Jupyter Lab!

* For JetRacer package update, execute following command.
```
cd jetracer
git checkout master
sudo python3 setup.py install
sudo reboot
```

### Load trained model

**Upload mean image** 

`/datasets/mean_image.npy`

**Upload trained model** 

`/checkpoints/resnet18.pth`

### Run

*Code :* `JetRacerRun.ipynb`

1. Import *nvidia_racecar*, *csi_camera* by `Cell 1` 
2. Create & load model by `Cell 4`
3. Read image from the camera, preprocess the image
4. Compute current pose using your model

### Demo

<p align="center"><img src="https://github.com/e-LENS/JetRacer/assets/79262676/b09d9908-13cf-4824-b67c-3cdc627431f4"></p>
<p align="center"><em>Ewha W. University, Asan Building, 2F</em></p>
