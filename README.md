# django-blog

1、下载源代码到本地

使用git命令下载
git clone https://github.com/Bgods/Django-blog-material-x.git
或者点击下载到本地
2、修改配置

修改 www/www/settings.py 文件

#  邮箱配置
EMAIL_USE_SSL = True
EMAIL_HOST = 'smtp.163.com'  # 我这里使用的是163邮箱，可以配置其他
EMAIL_PORT = 465
EMAIL_HOST_USER = 'bgods_blog@163.com'  # 邮箱帐号：用于发送邮件的账号
EMAIL_HOST_PASSWORD = '******'        # 邮箱密码：用于发送邮件的账号密码
DEFAULT_FROM_EMAIL = 'bgods_blog <bgods_blog@163.com>'   # 发件人，邮件头部显示

EMAIL_RECEIVE_LIST = [
    'bgods@qq.com',
]  # 接收邮件帐号列表(可写多个)： 有评论时候，通知哪些邮箱，可以是发件邮箱或者其他
当然, 还有其他配置, 比如后台管理以及评论内容编辑器的配置, 具体自己可以百度调整

3、安装依赖

进入项目目录创建虚拟环境，安装依赖
cd Desktop/www # 进入项目目录
virtualenv venv # 创建虚拟环境
source venv/bin/activate # 激活虚拟环境
pip install -r requirements.txt # 安装依赖


4、收集静态文件

python manage.py collectstatic
5、创建数据库

python manage.py makemigrations
python manage.py migrate


6、创建超级管理员账号

python manage.py createsuperuser
依次输入用户名，邮箱，密码



7、运行

python manage.py runserver 127.0.0.1:9000
运行上面代码，本地访问 127.0.0.1:9000 就能看到你的站点了。

8、其他问题

静态文件：
路径 www/static 下存放的js、css、font，以及站点的logo等图片，logo等图片可以替换自己的；
