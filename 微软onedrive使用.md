# 注册

两种方法  
1. 教育邮箱注册,自动5T  网址
    - [学生版账号注册地址](https://signup.microsoft.com/signup?sku=student)
    - [教师版账号注册地址](https://signup.microsoft.com/signup?sku=faculty)
2. 365 E5 开发者注册,默认1T, 可升5T
    - [365 E5 开发者注册](https://developer.microsoft.com/zh-cn/office)  
    - [下载微软shell工具修改5t](https://www.microsoft.com/zh-CN/download/details.aspx?id=35588)  
```
# 域名修改成你的域名
Connect-SPOService -Url https://域名-admin.sharepoint.com
# 登录你的账号,onmicrosoft.com的账号
# 用户名@域名.onmicrosoft.com
Set-SPOSite -Identity https://域名-my.sharepoint.com/personal/用户名_域名_onmicrosoft_com -StorageQuota 5242880
```
# 登录
[登录账号地址](https://login.microsoftonline.com)

# oneindex
[Github地址](https://github.com/donwa/oneindex)  
- 可以docker安装
- 也可以通过宝塔配置网页

1. 安装宝塔面板与建站依赖

2. 域名解析到服务器

3. 复制下载链接，远程下载并解压到网站根目录.

修改 contrer 目录下 AdminController.php 为自己的域名（line186）  
```
# 保证网址支持https
php $redirect_uri = 'https://oneindex.github.io/';  
```

重要的步骤, 从azure获得client和secrets.  
  
[登录地址](https://portal.azure.com/)

![](https://raw.githubusercontent.com/LinCheungS/PicGo_Image_Storage/master/2020/20200422062151.jpg)  
这一步权限记得确认,授予管理员同意  
![](https://raw.githubusercontent.com/LinCheungS/PicGo_Image_Storage/master/2020/20200422062225.jpg)  
![](https://raw.githubusercontent.com/LinCheungS/PicGo_Image_Storage/master/2020/20200422062549.jpg)
- 保证https
- 保证azure中的网址和AdminController.php修改的一样

oneindex后台- ?/admin  
view/admin/layout.php 修改跳转到官方后台  

[可选]**推荐配置**，非必需。后台定时刷新缓存，可增加前台访问的速度。  
```
# 每小时刷新一次token
0 * * * * /具体路径/php /程序具体路径/one.php token:refresh

# 每十分钟后台刷新一遍缓存
*/10 * * * * /具体路径/php /程序具体路径/one.php cache:refresh
```