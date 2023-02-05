### 功能

1. 邮件提醒
2. 每日天气
3. 每日鸡汤
4. 每日博客
5. 增删改查用户


#### 命令
1. -l 查看所有用户
2. -a [name] [mail] [city]添加一个用户 如果[mail]已存在，则视为修改
3. -d [mail] 删除一个用户
4. -h 查看帮助


#### 天气api


 ```url
 http://toy1.weather.com.cn/search?cityname=北京   通过此接口查询到城市id
 http://www.weather.com.cn/weather1d/{城市id}.shtml 
 ```


#### 鸡汤api

 ```url
 https://tool.lu/timestamp/
 ```

#### 博客api

 ```url
 https://www.oschina.net/blog
 ```

#### 设置定时发送邮件
linux 的 crontab 命令 ，每天的8：30发送邮件
crontab -e 进入编辑 ， 内容如下

```sh
SHELL=/bin/bash
PATH=/sbin:/bin:/usr/sbin:/usr/bin
MAILTO=root
HOME=/
30 8 * * * java -jar /root/dailymail.jar
```
