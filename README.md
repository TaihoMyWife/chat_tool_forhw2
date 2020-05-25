
===========================
###########环境依赖
系统环境：centos 7
内核版本：linux 4.15.0
###########部署步骤
1. 安装python2

2.下载内核源码：
    （1）git clone https://github.com/taihomywife/pychat.git

3. 安装 pip，pyaudio，pyqt4 
########### 执行选项
1. |--make client //启动客户端
   |--make server //启动服务器端
   |--make clean // 清除pyc文件
   |--make cleanup //清除环境

###########目录结构描述
├── demo               //账号信息
|   ├──user
|   ├──client      
├── doc                // 日志文件
├── client                     // 客户端
│   ├── main.py                // 主界面
│   ├── ui_chat.py             // 聊天窗
│   ├── ui_login.py            // 登录
│   ├── ui_regist.py           // 注册
│   ├── img_src.py             // 图像二进制流(utf-8)
│   ├── img                    // 图像素材库 
|   ├── net.py                 // 发送信息,监听端口.更新 
├── server                     // 服务器端
│   ├── const.py               // 常量
│   ├── daemon.py              // 多进程(抄的，下面有相关借鉴资料)
│   ├── friends.py             // 好友检索
│   ├── message.py             // 消息发送
│   ├── server.py              // 服务器主程序
│   ├── logger.py              // 抄的附赠 
|   ├── utils.py               // 抄的附赠  
├── demo                    // 记录
│   └── msg                 // 消息记录
│   └── user                // 用户记录
###########代码参考
Author:         http://www.jejik.com/articles/2007/02/
                        a_simple_unix_linux_daemon_in_python/www.boxedice.com