
# 安装 宝塔 面板

- [宝塔官网](https://www.bt.cn/)
```
curl -sSO http://download.bt.cn/install/new_install.sh && bash new_install.sh
```

- 修改端口，登录名密码
- /www/wwwroot/lin233.fun/wp-content/themes 删除主题
- 设置静态网页,加快加载速度

# 安装 WordPress

## wordpress插件
- WP Editor.md - 支持markdown
- Hermit X - 基于 Aplayer 的播放器
- WP Super Cache - 生成缓存加快访问


## 樱花庄的白猫
[官方示例](https://2heng.xin/theme-sakura/)  
[Sakura](https://github.com/mashirozx/Sakura)  
- 修改图库
    - 第一屏选择内置原图随机图
    - 上传至 /www/wwwroot/lin233.fun/wp-content/themes/Sakura-3.3.7/manifest/gallary  
- 生成文章目录
    - 在需要目录的文章任意位置输入 [toc] 启用
- 背景过滤图选网格
- 关闭聚焦  

## 搭建网址导航webstack
[WebStackPage - 静态网页版](https://github.com/WebStackPage/WebStackPage.github.io)  
[WebStack - worldpress版](https://github.com/owen0o0/WebStack)  
- worldpress中- 网址 - 网址分类 # 修改左侧导航
- [左侧图标](https://fontawesome.dashgame.com/) 用法fa-名字
- 网址-添加网址,添加具体的网站
- url/favicon.ico 获取图标
- 不用的东西看感觉删php代码
- 修改主题logo 2x.png
