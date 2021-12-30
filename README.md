# live_comment_control_stream

接收弹幕指令并控制电脑操作 Python3+Redis+PyAutoGUI

## 实现原理

通过Github作者的项目

https://github.com/wbt5/real-url

获取直播实施弹幕

将弹幕写入消息队列

消费者接受消息，将弹幕内容转为键盘指令，最终通过PyAutoGUI操作电脑

## 代码结构

- control
    - consumer.py
    - display_redis.py
    - pyautogui_test.py
- danmu: 此文件夹代码取自https://github.com/wbt5/real-url
    - danmaku:各平台弹幕获取
    - main.py
## 使用方法
1.下载这个仓库（推荐Pycharm运行）  
2.安装requirements.txt依赖

    pip install -r requirements.txt

3.下载并安装Redis
https://github.com/MicrosoftArchive/redis/releases

4.修改main.py里的直播间地址以及你玩游戏的按键  
key_list就是按键列表  
consumer.py里也要修改

5.打开bilibili并用obs推流
https://link.bilibili.com/p/center/index#/my-room/start-live  
6.依次启动  
main.py  
display_redis.py  
consumer.py  
7.打开你要玩的游戏
## 其他
代码来自
https://github.com/qqxx6661/live_comment_control_stream  
实现思路  
https://www.cnblogs.com/rude3knife/p/15635306.html

