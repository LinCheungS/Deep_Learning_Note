# 编译Lean OpenWrt路由刷机
[Lean Github](https://github.com/coolsnowwolf/lede)  
[OpenWrt 型号查询](https://openwrt.org/docs/techref/targets/start)  
[官方仓库](https://downloads.openwrt.org/releases/)

# 注意事项
1. 硬盘要足够大
2. 非root用户
3. 插件选的太多会不生成squashfs-sysupgrade.bin，M单独编译
4. 

# 准备工作
```
#切换到root角色
sudo -i 
#修改SSH配置文件
vi /etc/ssh/sshd_config
#修改PermitRootLogin和PasswordAuthentication
PermitRootLogin yes 
PasswordAuthentication yes
#给root用户设置密码
passwd root
#重启SSH服务使修改生效
/etc/init.d/ssh restart

passwd lincheung0
su lincheung0
sudo apt-get update
```
切换root用户  
sudo vi /etc/sudoers  
Then add the user below admin user like below syntax.  
user_name ALL=(ALL)  ALL  
切换到用户账号  
```
sudo apt-get -y install build-essential asciidoc binutils bzip2 gawk gettext git libncurses5-dev libz-dev patch python3.5 unzip zlib1g-dev lib32gcc1 libc6-dev-i386 subversion flex uglifyjs git-core gcc-multilib p7zip p7zip-full msmtp libssl-dev texinfo libglib2.0-dev xmlto qemu-utils upx libelf-dev autoconf automake libtool autopoint device-tree-compiler g++-multilib linux-libc-dev:i386
```
Unable to locate package libc6-dev-i386  
用libc6-dev替换
```
sudo apt-get -y install build-essential asciidoc binutils bzip2 gawk gettext git libncurses5-dev libz-dev patch python3.5 unzip zlib1g-dev lib32gcc1 libc6-dev-i386 subversion flex uglifyjs git-core gcc-multilib p7zip p7zip-full msmtp libssl-dev texinfo libglib2.0-dev xmlto qemu-utils upx libelf-dev autoconf automake libtool autopoint device-tree-compiler g++-multilib libc6-dev

sudo apt-get install screen
#防止断开连接
screen -dmS aaa 
# 记得用非root用户登录ssh
screen -ls
screen -r
git clone https://github.com/coolsnowwolf/lede 
cd lede
./scripts/feeds update -a 
./scripts/feeds install -a
make menuconfig
```
选好你的路由固件  
ssr全部勾选  
参考[OpenWrt 型号查询](https://openwrt.org/docs/techref/targets/start) 

```
make -j1 V=s
```
编译好的在bin目录