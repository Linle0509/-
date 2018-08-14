# -*- coding: utf-8 -*-
import itchat
import time
Wchat = itchat.auto_login(hotReload=True)   #   保持登录状态 
friends_list = itchat.get_chatrooms(update=True)     #  获取群聊   获取好友则为get_friends()
name = itchat.search_chatrooms(name=u'牛逼一群')        #   搜索群name
Name = name[0]['UserName']
while True:
    time_now = time.strftime('%H%M', time.localtime(time.time()))  
    if int(time_now) == 100:
        message_content = '为群站岗'
        itchat.send(message_content, Name)
        time.sleep(3600)
        message_content = '有没有能打的？'
        itchat.send(message_content, Name)
        time.sleep(3600)
        message_content = '一个能打的都没有？'
        itchat.send(message_content, Name)
        time.sleep(3600)
        message_content = '垃圾'
        itchat.send(message_content, Name)
        time.sleep(3600)
        message_content = '为群站岗'
        itchat.send(message_content, Name)
