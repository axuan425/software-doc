# centos install
```
yum install -y docker
vi /etc/docker/daemon.json
```

> {
  "registry-mirrors": [
    "https://registry.docker-cn.com",
    "http://hub-mirror.c.163.com",
    "https://docker.mirrors.ustc.edu.cn"
  ]
}

```
systemctl restart docker
```

# For use
### get mount dir for container
> docker inspect <container_id> | grep Mounts -A 20

