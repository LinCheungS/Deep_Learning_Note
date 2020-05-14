# 测速脚本
```bash
wget -qO- --no-check-certificate https://raw.githubusercontent.com/oooldking/script/master/superbench.sh | bash
```

# TCP加速(四合一)
```bash
wget "https://github.com/chiakge/Linux-NetSpeed/raw/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh

wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubiBackup/doubi/master/bbr.sh && chmod +x bbr.sh && bash bbr.sh
```

# SSR
```bash
wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubiBackup/doubi/master/ssr.sh && chmod +x ssr.sh && bash ssr.sh
```

# aria2 && ariang
> sudo 环境下

```bash
apt-get install nginx -y
systemctl start nginx
systemctl enable nginx.service
iptables -L
```
```bash
wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubi/doubi/master/aria2.sh && chmod +x aria2.sh && bash aria2.sh
mkdir -p /data/download     #mkdir 修改一下下载路径
./aria2.sh      #修改为 /data/download
mkdir -p /data/www/ariang && cd /data/www/ariang
apt-get install unzip
wget https://github.com/mayswind/AriaNg/releases/download/1.1.0/AriaNg-1.1.0.zip && unzip AriaNg-1.1.0.zip
rm -rf AriaNg-1.1.0.zip 

cd /etc/nginx/conf.d && touch ariang.conf
vim ariang.conf
server {
    listen 80;
    server_name <IP_ADDRESS>;
    location / {
        root   /data/www/ariang;
        index  index.html index.htm;
    }
}

systemctl reload nginx
```
 地址   : 
 端口   : 6800
 密码   : a0ef32c6a53d57765108
 目录   : /data/download
 
# plex
```bash
wget https://downloads.plex.tv/plex-media-server-new/1.15.4.994-107756f7e/debian/plexmediaserver_1.15.4.994-107756f7e_amd64.deb && dpkg -i plexmediaserver*.deb

systemctl enable plexmediaserver.service && systemctl start plexmediaserver.service

ssh lincheung0@34.74.167.243 -L 8889:localhost:32400

localhost:8889/web
```
 
