# MobiBot
### Abstract

## Table of content

## Hardware
### Components
Components used in this project:
| Part No.|Part|Status
| ---| ---|---|
|1| [Raspberry Pi 4 (8GB)](https://www.electrokit.com/en/raspberry-pi-4-model-b/8gb)| 🔵 _Acquired_ |
|2| 2 x [Motors with encoders](https://www.amazon.se/dp/B07WP3XDLC?psc=1&ref=ppx_yo2ov_dt_b_product_details)|🔵 _Acquired_ |
|3| [RPLiDAR A1](https://www.mouser.se/ProductDetail/426-DFR0315)| 🔵 _Acquired_ |
|4| [Caster wheel](https://www.mouser.se/ProductDetail/485-3948)| 🔵 _Acquired_ |
|5| [DC-DC converter Step-down](https://www.electrokit.com/en/dc-dc-omvandlare-step-down-1.25-35v-5a)|🔵 _Acquired_ |
|6| [Motor driver L298 dual H-bridge 5-35V 2A](https://www.electrokit.com/en/motordrivare-l298-dubbel-h-brygga-5-35v-2a)|🔵 _Acquired_ |
|7| [3000mAh 3S 20C Lipo Pack w/XT-60](https://hobbyking.com/en_us/turnigy-battery-3000mah-3s-20c-lipo-pack-xt-60.html)|🔵 _Acquired_ |
|8| [Lipo Charger](https://www.amazon.se/-/en/gp/product/B087G199LH/ref=ewc_pr_img_1?smid=ADG7ML0RBF414&psc=1)| 🔵 _Acquired_ |
|9| [Arduino Uno R3](https://www.mouser.se/ProductDetail/SparkFun/DEV-11021?qs=WyAARYrbSnaunJRU8m2iHw%3D%3D)|🔵 _Acquired_ |
|10| [Fuse holder](https://www.conrad.se/sv/p/tru-components-tc-9070404-sakringsinsats-passar-till-flatsakring-standard-30-a-32-v-dc-1-st-2267601.html)|🔵 _Acquired_ |
|11| [Fuse](https://www.conrad.se/sv/p/eska-340127-340-127-standardflatsakring-10-a-rod-1-st-535104.html)|🔵 _Acquired_ |
|12| [Toggle switch](https://www.conrad.se/sv/p/tru-components-1587656-vippstrombrytare-tc-r13-244b-02-b-r-220-v-ac-250-v-ac-10-a-2x-av-pa-lasande-1-st-1587656.html)|🔵 _Acquired_ |
|13| Jumper cables|🔵 _Acquired_ |
|14| 22 AWG wires|🔵 _Acquired_ |
|15| [MPU6050 IMU](https://www.mouser.se/ProductDetail/426-SEN0142)| 🔵 _Acquired_ |
|16| [3D-printed parts]()| 🔵 _Acquired_ |
|17| [SD-card 64GB](https://www.inet.se/produkt/5304540/samsung-microsd-evo-plus-64gb)|🔵 _Acquired_ |
### Legend

- 🔵 **Blue:** Components acquired
- 🟢 **Green:** Parts ordered
- 🟡 **Yellow:** Additional accessories pending
- 🔴 **Red:** Review needed before purchase
- 🟣 **Purple:** 3D-printed parts in production

Useful tools
|| Tool |
| --| --|
|1| Soldering iron|
|2| 3D-printer|
|3| Multimeter|
|4| Lab-bench power supply|

### Assembly
Current draw is approx 0.5A
### Setup
## Development machine
## Raspberry Pi setup
### Format SD card
Download the [raspberry pi imager](https://www.raspberrypi.com/software/) for your system. Launch the program and follow the instructions. Choose "other os" then Ubuntu server 22.04 LTS. Modify any settings youd like, I suggest setting up the internet and enabling ssh.
### Find the IP-address of the raspberry pi using [nmap](https://nmap.org/)
1. First install nmap on your system that you want to use to connect to the raspberry pi.
2. If you are running linux, run ```ip addr``` to find your machines IP address and the network range.
3. Run ```sudo -ns 192.168.1.x/24```(replace x and 24 with the correct values for your setup)
4. Identify your raspberry pi. If it does not show, you can try to just ssh to all the hosts. In my case it was named
```
MAC Address: xx:xx:xx:xx:xx:xx (Huawei Technologies)
nmap scan report for 192.168.1.30
```
### Installing ROS2 Humble
Follow the steps given [here](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html) to install ROS2 humble on your raspberry pi. Depending if you installed the OS on the raspberry pi in headless mode or desktop mode, ```ros-humble-base```and ```ros-humble-desktop``` should be installed respectively.

Next we need to install the colcon build package.
```bash
sudo apt install python3-argcomplete python3-colcon-common-extensions libboost-system-dev build-essential
```
I recommend to append the following to your bashrc:
```bash
echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc
```
## Network Configuration
## Differential drive controller
## SLAM
## Navigation
## Simulation
### Gazebo
### URDF model
