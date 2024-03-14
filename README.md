# wenz

首先展示效果图
![image](https://github.com/evilsnlan/wenz/assets/61233992/94758b76-0a4b-4521-bb64-8851b2546fb1)

该漏洞是在后台呈现的，需要登陆后台，首先我们搭建网站，版本为2.2.9，注册管理员，进入后台
![image](https://github.com/evilsnlan/wenz/assets/61233992/04f080fb-34f2-4f57-9d23-0be15ec9c337)
然后进入user.php，手动添加3个注册用户
![image](https://github.com/evilsnlan/wenz/assets/61233992/dac4e904-4672-4b6b-8630-1ba354fa19b4)
可以看到，注册用户的名字是随机的，接下来，进去data.php，备份出用户数据
![image](https://github.com/evilsnlan/wenz/assets/61233992/49423131-4587-4a44-9655-7bef7a73332a)
![image](https://github.com/evilsnlan/wenz/assets/61233992/9ed0b6a6-c775-4479-a4af-84160e881124)
然后修改name字段为sql语句
![image](https://github.com/evilsnlan/wenz/assets/61233992/1878f850-d10f-44cc-b2de-3bf6d7f6fcbb)
保存文件，并进行导入
显示已经成功
![image](https://github.com/evilsnlan/wenz/assets/61233992/74fa129d-8f25-4910-9a41-573b2931e09f)
这时我们去user.php查看，发现用户名已经执行了对应的sql语句
![image](https://github.com/evilsnlan/wenz/assets/61233992/cbc55031-76b7-4847-853f-5d45e300ad9b)
原因是data.php在导入数据的时候没有进行严格的过滤
