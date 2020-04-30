# xadmin-django3.0
 调整后适用于django3.x版本的xadmin <br>

# xadmin简介
 将Django自带的admin系统替换，提供了其他实用的东西；而且完全的可扩展的插件支持，并且是基于Twitter Bootstrap的漂亮UI。<br>
 原项目地址https://github.com/sshwsfc/xadmin

# xadmin的坑
 xadmin 0.6.0 和0.6.1分别支持django1.9与django2.x版本。导致在新版django使用不便,需要做诸多调整。<br>
# 安装
#### 工具pychram
 - 下载该zip,解压为文件夹复制到工程extra_apps目录下,并将extra_apps设置为Source Root<br>
 - 前往setting.py文件里的INSTALLED_APPS下做好配置<br><code>
 'xadmin',
    'crispy_forms',
    'reversion',
    'django.conf'
 </code><br>
 其中部分依赖crispy_forms和django_reversion可能需要单独使用pip安装
 - django3.x移除了在django/utils包下的six.py,需要使用命令<br><code>
  pip install six
 </code><br>
 执行<code>pip show six</code>和执行<code>pip show django</code>查看django安装目录，
 并将six.py拷贝至django/utils包下。six.py需要添加部分方法,拷贝下载后的压缩包里的six.py内容至python安装的six.py内容。
# 运行使用
运行可以完全参照https://xadmin.readthedocs.io/en/latest/index.html  
使用完全可以参照https://www.jianshu.com/p/49eb568c9a25
# 其他问题排查
富文本使用失效参考链接https://blog.csdn.net/xiaosongshine/article/details/88548348  
每次登录管理员用户前请先切换为django自带的login界面登录,再切换为自己的。