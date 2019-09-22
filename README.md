# HeNavigation
**这是一个基于Django的网址导航**

**效果图**
![效果图](http://doc.hfybbs.vip/server/../Public/Uploads/2019-09-22/5d87726e9a91c.png "效果图")

[演示站](http://newdh.hfybbs.vip "演示站")

**使用方法**
**测试系统：Ubuntu**
### 使用之前请事先安装python3，Django，Mysql/mariadb，mysqlclient/pymysql
```python
sudo apt-get install python3 python3-pip mariadb-server mariadb-client
pip3 install django mysqlclient
```

> 下载HeNavigation-backup.zip文件，并解压进入目录，配置HeNavigation/setting.py文件

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': '你的数据库名',
        'USER': '数据库用户名',
        'PASSWORD': '数据库密码',
        'HOST':'localhost',
        'PORT':'3306',
    }
}
```

> 在HeNavigation-backup目录下，执行命令


```python
python3 manage.py makemigrations
python3 manage.oy migrate
```

> 再执行命令添加管理员账号，依次输入账号，邮箱，密码，确认密码

```python
python3 manage.py createsuperuser
```

> 最后运行服务

```python
python3 manage.py runserver 0.0.0.0:9000
```

**最后访问http://ip地址:9000**
**管理面板地址为：http://ip地址:9000/admin**
**刚搭载起来是一片空白，自己去管理面板添加即可**
管理面板说明：

| 类名  |  说明 |
| ------------ | ------------ |
|  Classification |  分类 |
|  Navigation |  导航网址 |
