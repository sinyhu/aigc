# 发型服务的启动流程及命令记录

## 启动换发型的服务
cd /mnt/datadisk/workspace/mz_hair && conda activate condiff-train-hair && export CRYPTOGRAPHY_OPENSSL_NO_LEGACY=1 && CUDA_VISIBLE_DEVICES=0 python run_copy_cost.py 

## 启动训练发型的服务
cd /mnt/datadisk/workspace/photo_service && conda activate py310 && CUDA_VISIBLE_DEVICES=0  python lora_train_service_1.py 

## 启动webui的服务器
cd /mnt/datadisk/workspace/onediff/stable-diffusion-webui && conda activate onediff &&CUDA_VISIBLE_DEVICES=1 ./webui.sh --api --listen --disable-safe-unpickle --port 57860
cd /mnt/datadisk/workspace/onediff/stable-diffusion-webui && conda activate onediff && CUDA_VISIBLE_DEVICES=0 ./webui.sh --api --listen --disable-safe-unpickle --port 57861

