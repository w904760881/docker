## 本地安装Docker虚拟机

1.先安装DockerToolbox-19.03.1.exe

```
环境变量配置
DOCKER_TOOLBOX_INSTALL_PATH：C:\Program Files\Docker Toolbox\
VBOX_INSTALL_PATH：C:\Program Files\Oracle\VirtualBox\
VBOX_MSI_INSTALL_PATH：C:\Program Files\Oracle\VirtualBox\
```

2.安装VirtualBox-6.1.4-136177-Win.exe

3.打开VirtualBox，会显示虚拟机default正在运行

```
docker 配置环境变量
path 下面添加配置 C:\Program Files\Docker Toolbox
```

4.打开Cmder

```
docker ps --查看docker下面的image
docker pull openjdk：8-alpine --获取openjdk
docker images --可以查看openjdk了
docker-machine.exe ssh --登录本地虚拟机
cd /etc/docker  --到docker目前下面
sudo touch daemon.json --创建一个daemo.json文件
sudo vi daemon.json --打开daemon.json文件把
  {                                                                                                    "insecure-registries":["registry.schindlerioee.com","10.69.94.140:5000"]
  }  
  复制到文件中，保存退出 ：wq
cat daemon.json --查看文件内容
sudo /etc/init.d/docker restart --重启


```

5. 获取一个sms-dateway实例

   ```
   docker pull 10.69.94.140:5000/sms-gateway:2020-04-15 --拉取一个sms-gateway:2020-0415版本
   docker images --查看

   ```

   ​

