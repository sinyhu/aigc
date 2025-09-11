# omnigen voicefun dragmagic sdk 合并后验证

# voicefun 的处理记录
## 1、切换环境
* source ~/sidatian/SlowAI/env/bin/activate
  
## 2、启动api服务
* cd /root/music/web_service
* nohup python3 /root/music/web_service/main.py > /root/music/web_service/web_service.log 2>&1 &  启动api服务  服务端口32000
* cd /root/music/model_service
* nohup python3 /root/music/model_service/main.py > /root/music/model_service/model_service.log 2>&1 &  启动clone和训练模型任务

![img_v3_02q0_8af19216-3d89-4e18-b020-9399a2d96dfg](https://github.com/user-attachments/assets/8d48c42d-aaa7-41fd-8b88-4a1b03e16290)
迁移过程中遇到引用错误
在代码中加入
vim /root/music/model_service/main.py
sys.path.insert(0,'/root/sidatian/VoiceFun/src/libs')

# dragmagic 的处理记录
## 1、切换环境
* source ~/sidatian/SlowAI/env/bin/activate
  
## 2、启动api服务
* cd /root/drag/web_service
* nohup python3 /root/drag/web_service/main.py > /root/drag/web_service/web_service.log  2>&1 &  启动api服务 服务端口32001
* cd /root/drag/model_service
* nohup python3 /root/drag/model_service/main.py > /root/drag/model_service/model_service.log  2>&1 &
 

# omnigen 的处理记录
## 1、切换环境
* source ~/sidatian/SlowAI/env/bin/activate

## 2、启动api服务
* cd /root/package/omnigen/web_service
* nohup python3 /root/package/omnigen/web_service/main.py > /root/package/omnigen/web_service/web_service.log  2>&1 &  启动api服务  服务端口32002
* cd /root/package/omnigen/model_service
* nohup python3 /root/package/omnigen/model_service/main.py > /root/package/omnigen/model_service/model_service.log  2>&1 &
  


