# JetRacer

### Environment Setting

### How to use

1. Connect to wireless network in Jetson Nano & your computer
2. Access Jupyter Notebook by http://172.20.10.10:8888/
3. Execute JetsonRun.ipynb 
4. 

### Demo

# Hardware

## Requirements
* Jetson Nano 2GB Developer Kit
* Jetracer
* micro SD card (64GB~)
* balenaEtcher

## Installation

1. 사용할 micro SD card 포맷
2. Jetson Nano Image
* [jetson-nano-2gb-sd-card-image](https://developer.nvidia.com/jetson-nano-2gb-sd-card-image) 다운로드 및 압축 해제
* Etcher 프로그램으로 microSD card에 Jetson Nano Image write
* Jetson nano의 SD card slot에 SD card를 넣은 후, HDMI 포트를 통해 모니터 연결 및 system configuration 설정
3. JetRacer Image
* [JetRacer image](https://drive.google.com/file/d/1YtnjQ77w1B9REzy1JgLJbVSs2K3ocAEr/view?usp=sharing) 다운로드 및 압축 해제
* Etcher 프로그램으로 microSD card에 Jetracer Image write
* Jetson nano의 SD card slot에 SD card를 넣은 후, HDMI 포트를 통해 모니터 연결 및 system configuration 설정

(+)
* GUI가 비활성화 되어있다면 `sudo systemctl set-default graphical.target` command 실행

## Connect to JetRacer

1. WIFI에 JetRacer 연결
2. Jetson Nano의 piOLED 또는 `ifconfig` command 로 Wlan0 interface의 ip address 확인
3. 이후 브라우저에서 `http://<ip address>:8888` 주소로 RetRacer에 무선 연결
4. Password `jetbot` 을 입력해 Jupyter Lab 실행

* JetRacer package 업데이트를 위해서 다음 command 실행
```
cd jetracer
git checkout master
sudo python3 setup.py install
sudo reboot
```
