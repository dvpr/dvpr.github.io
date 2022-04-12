## 树莓派
> Raspberry Pi

<br><br>

##### 国内镜像站

```
[TUNA 镜像站（北京）](https://mirrors.tuna.tsinghua.edu.cn/raspberry-pi-os-images)
[SJTUG 镜像站（上海）](https://mirrors.sjtug.sjtu.edu.cn/raspberry-pi-os-images)
```

<br><br>

##### 安装桌面环境
##### Install Desktop for Lit OS

```
sudo apt install xserver-xorg -y //install Xorg
sudo apt install raspberrypi-ui-mods -y // install default Desktop Environment
sudo apt install lightdm -y // restart on boot
sudo reboot
```

<br><br>

##### 桌面环境开机启动软件
##### Run software on boot on Desktop
```
sudo vi /etc/xdg/autostart/your_script_name.desktop

[Desktop Entry]
Name=Play a video
Exec=mpv --fs your_video_path
```