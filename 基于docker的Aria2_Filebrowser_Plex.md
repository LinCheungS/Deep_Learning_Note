BT下载+流媒体播放  
项目源地址：[aria2-ariang-x-docker-compose](https://github.com/wahyd4/aria2-ariang-x-docker-compose)

## 安装docker 和 Docker Compose
[debian docker 系统的官方教程](https://docs.docker.com/install/linux/docker-ce/debian/)  
[Linux Docker Compose 官方教程](https://docs.docker.com/compose/install/#install-compose)

### 设置docker存储库
```
# 1. 更新apt包索引
sudo apt-get update

# 2. 安装软件包以允许apt通过HTTPS使用存储库
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg2 \
    software-properties-common
    
# 3. 添加Docker的官方GPG密钥
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -

# 4. 设置存储仓库
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/debian \
   $(lsb_release -cs) \
   stable"
```
### 安装DOCKER ENGINE - COMMUNITY

```
# 1. 更新apt包索引。
sudo apt-get update

# 2. 安装最新版本的Docker Engine
sudo apt-get install docker-ce docker-ce-cli containerd.io

# 3. 运行hello-world验证是否正确安装
sudo docker run hello-world
```
### 安装Docker Compose

```
# 下载
sudo curl -L "https://github.com/docker/compose/releases/download/1.25.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

# 权限
sudo chmod +x /usr/local/bin/docker-compose

# 测试
docker-compose --version
```

## 安装aria2-ariang-Filebrowser-plex
项目源地址：[aria2-ariang-x-docker-compose](https://github.com/wahyd4/aria2-ariang-x-docker-compose)

```
# 从github上克隆项目
git clone https://github.com/wahyd4/aria2-ariang-x-docker-compose.git

# 进入指定路径
cd aria2-ariang-x-docker-compose/plex-filebrowser

# 前往 https://www.plex.tv/claim/ 获取 TOKEN， 
# 并填充至 `plex-filebrowser` 目录下的 `docker-compose.yml`下的 `PLEX_CLAIM`字段

# 安装
docker-compose up -d
```
![1](https://tva4.sinaimg.cn/large/a17dfad9ly1gc5o092ph7j20pj0k174v.jpg)

**进入以下端口访问**
1. Filebrowser http://localhost （默认账号密码admin）
2. AriaNg： http://localhost/ui
3. Plex: http://localhost:32400

## 注意事项

### 1. aria2 更新tracker
[github.com/ngosang/trackerslist](https://github.com/ngosang/trackerslist)

### 2. plex第一次进入需要本地转发

```
ssh root@服务器IP -L 8888:localhost:32400

# 登陆后，浏览器里打开localhost:8888/web进入即可
# 登入plex账号后，以后可用公网ip访问
```
