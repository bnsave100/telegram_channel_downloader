
just random translation credits to original dev https://github.com/snow922841/

# telegram_channel_downloader
Telegram channel/group file download script

The script needs python3 environment,the specific installation tutorial to search for itself.

Test environment Ubuntu 18.04.5 LTS & Python 3.6.9
**1. Premise**
 
 - ~~安装redis~~
 
   ~~安装教程参考 [Redis 安装 | 菜鸟教程](https://www.runoob.com/redis/redis-install.html)~~
 
 
 - 从 https://my.telegram.org/apps 获取自己的Telegram API密钥。

- Download script
```
git clone https://github.com/snow922841/telegram_channel_downloader.git
```

**2. Use**

- Go to the script directory
```
cd telegram_channel_downloader
```
- Install dependencies

```
pip3 install -r requirements.txt
```

- Modify telegram_channel_downloader.the api_id and api_hash inside the PY File are your own

- Modify the required configuration of Channel Name, save path, bot_token, admin_id, chat, etc. in the script

- In view of the user needs to upload GD,added the use of gclone automatically uploaded to the team disk function, you need to configure the regional settings.View the comments in the script specifically

- Run
```
python3 tg_channel_downloader.py
 ```
 - Follow the prompts to enter the telegram bound phone number to get the verification code and enter

- After the configuration is complete, you need to send a link to the bot /start Channel 0 to officially start running the script, otherwise you can not start 0 on behalf of the ID to start downloading the message, you can modify it yourself.
 
<details>
  <summary>点击查看更新日志</summary>
 
  2020-09-15更新
  
   - 移除下载上传进度条显示。
   
   - 使用异步并发，默认10个任务同时进行。
   
   - 修复异常重试
   
   - 远程添加任务，方便下载多个频道消息。
   
   - 移除redis保存任务
   
   - 增加全部频道、群组新消息监控，请在配置区域自行修改。
    
  2020-09-03更新
  
   - ref超时异常自动重试
  
  2020-09-01更新
  
   - 使用bot启动，并使脚本持久化，
   
   - 优化代码
   
   - 修复一些bug
  
  2020-08-29更新
  
   - 更换telegram的第三方库
  
   - 默认上传到GD，目前未配置不上传，所以需要安装gclone
  
   - 默认过滤贴纸、动态贴纸、gif格式文件
  
   - 优化了下载和上传进度条的显示
  
   - 上传失败后会把消息ID保存在脚本所在的文件夹，方便以后可以手动下载
  
  2020-08-19更新
     
   - 添加自动上传到Googledrive的功能
     
   - 使用redis缓存已经遍历的消息ID
 
</details>
