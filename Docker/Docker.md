## Docker

##### Docker清理空间
##### Clean

```
docker system prune -a
```

##### 查看Docker空间占用
##### df

```
docker system df
```

##### Docker ps 查看完整信息
##### Docker ps display the full command along

```
docker ps --no-trunc
```

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