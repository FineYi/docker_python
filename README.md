# docker_python

1. 本地安装
    - `git`
    - `Docker`(系统需为Linux，Windows 10 Build 15063+，或MacOS 10.12+，且必须要`64`位）
    - `docker-compose 1.7.0+`
2. 镜像加速：
    - Mac系统：
    
    ```
        依次点击docker图标->Preference->Docker Engine 在输入框输入如下内容：
        
        {
          "debug": true,
          "experimental": false,
          "registry-mirrors": [
            "https://4z24oo4j.mirror.aliyuncs.com",
            "http://hub-mirror.c.163.com",
            "http://f1361db2.m.daocloud.io"
          ]
        }
        
        点击：Apply & Restart
    ```
    
    - Linux系统：
    
    ```
        对于使用 systemd 的系统，请在 /etc/docker/daemon.json 中写入如下内容（如果文件不存在请新建该文件）
        
        {
          "registry-mirrors": [
            "https://4z24oo4j.mirror.aliyuncs.com",
            "http://hub-mirror.c.163.com",
            "http://f1361db2.m.daocloud.io"
          ]
        }
        
        之后重新启动docker服务
        sudo systemctl daemon-reload
        sudo systemctl restart docker
    ```
    
2. `clone`项目：
    ```
    $ git clone https://github.com/fineyi/docker_python.git
    ```
3. 如果不是`root`用户，还需将当前用户加入`docker`用户组：
    ```
    $ sudo gpasswd -a ${USER} docker
    $ 若上述命令执行失败，可以手动切换root用户后，再执行后续操作
    ```
4. 拷贝并命名配置文件（Windows系统请用`copy`命令），修改配置文件，启动：
    ```
    $ cd docker_python                                  # 进入项目目录
    $ cp env.sample .env                                # 复制环境变量文件
    $ vi .env
    $ 修改 SOURCE_DIR=物理机代码的绝对路径（用来映射到容器内部）
    $ cp docker-compose.sample.yml docker-compose.yml   # 复制 docker-compose 配置文件。默认启动1个服务：
                                                        # python361。要开启更多其他服务，如python27，请删
                                                        # 除服务块前的注释
    $ docker-compose up -d                              # 以后台运行方式启动
    ```
5.进入docker容器内部


```
$ docker exec -it python361 /bin/sh
$ cd /www                                               # 进入代码目录
$ 
```
