# discuz

全自动登录discuz论坛，签到，回帖刷币

## 环境
centos + python3.9

## 运行方式
 - 克隆仓库
 - discuz.py文件内修改论坛地址、账号、密码等信息

 ```
    hostname = ''   #论坛地址
    username = ''   #账号
    password = ''   #密码
```

 - 安装依赖，可以先直接运行 `python3 discuz.py`，缺哪个库装那个，直到日志（info.log）中显示登录成功的信息
 - crontab添加定时任务，每过6分钟执行一次回帖示例 `*/6 * * * * cd /root/discuz_bot/ && python3 discuz.py` 目录改成自己的

## 示例
![](demo.png)
 
## 说明
 - 自动识别验证码登录，也只能登录有验证码的论坛
 - 这只是针对某一个论坛写的代码，不一定对所有论坛都有效，但discuz论坛都类似，出错小改后基本就可以用了。