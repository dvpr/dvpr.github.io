## Docker

<br /><br />

##### Docker清理空间
##### Clean

```
docker system prune -a
```

<br /><br />

##### 查看Docker空间占用
##### df

```
docker system df
```

<br /><br />

##### Docker ps 查看完整信息
##### Docker ps display the full command along

```
docker ps --no-trunc
```

<br /><br />

##### 修改Docker主目录设置
##### Relocating the Docker root directory

###### 停止Docker服务
###### Stop the Docker services
```
systemctl stop docker
systemctl stop docker.socket
systemctl stop containerd
```

###### 修改Docker配置文件
###### Edit the file /etc/docker/daemon.json. If the file does not exist,just create it.
```
{
  "data-root": "/path_to_you_want/docker"
}
```

###### 启动Docker
###### Start the Docker services
```
systemctl start docker
```

###### 验证
###### Validate
```
docker info -f '{{ .DockerRootDir}}'
```

######

<br /><br />

##### 使用非root用户运行docker
##### Run the Docker daemon as a non-root user (Rootless mode)
> [链接](https://docs.docker.com/engine/security/rootless)

<br /><br />

##### 在树莓派中安装docker
##### How to install docker and docker-compose on Raspberry Pi

```
# Update source
sudo apt-get update && sudo apt-get upgrade

# Install docker by shell script
curl -sSL https://get.docker.com | sh

# Add user to docker group
sudo usermod -aG docker [user_name]
# Add current user to docker group
sudo usermod -aG docker ${USER}
# Check it
groups ${USER}

# Install docker-compose
sudo apt-get install libffi-dev libssl-dev
sudo apt install python3-dev
sudo apt-get install -y python3 python3-pip
sudo pip3 install docker-compose

# Enable docker service on boot
sudo systemctl enable docker

# Run hello world
docker run hello-world

# Upgrade
sudo apt-get upgrade

# Uninstall
sudo apt-get purge docker-ce
sudo apt-get purge docker-ce-cli
sudo rm -rf /var/lib/docker
```