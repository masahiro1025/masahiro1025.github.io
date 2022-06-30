# Docker



下載
```
docker pull {image_name}
```

尋找

```docker
docker search {image_name}
```

建立
```
docker run --name {NAME} -it -d -v {HostPATH}:{ContainerPATH} -p {HostPORT}:{ContainerPORT} --gpus {gpu_NUM} {image_name}
```

參數介紹

```
--name container的名字  
-v 設定主機哪個資料夾會被mount在container的哪裡  
-p 設定主機的PORT跟container對應  
-it -d 維持運行  
--gpus 設定給幾張GPU  
Image_name 放最後
```



建立範例
```

docker run --name cuda10 -it -d -v /home/user/workplace:/workplace -p 31025:22 --gpus all nviida/cuda:10.2-runtime-ubuntu18.04

```


啟動容器
```
docker run {ContainerNAME}
```

進入容器
```
docker exec -it {ContainerNAME} bash
```

參考資料
>裝Docker : https://blog.gtwang.org/virtualization/ubuntu-linux-install-docker-tutorial/  
>裝nvidia-Docker : https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html (非必要 但是要吃GPU要用這個比較方便)  
>找自己想要的 CUDA Image : https://hub.docker.com/r/nvidia/cuda/tags  

SSH教學
>https://bingdoal.github.io/deploy/2021/02/use-ssh-connect-on-docker-container/