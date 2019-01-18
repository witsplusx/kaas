


https://www.osyunwei.com/archives/9591.html
http://www.cnblogs.com/Berkaroad/p/6446059.html

现在客户端生成rsa 公钥密钥
ssh-keygen

通过虚拟机添加三个rancheros节点, 记录ip地址网关等   生成cloud-config.yml文件
sudo passwd rancher

拷贝到各个虚拟机节点
scp cloud-config.yml rancher@172.16.167.164:/home/rancher/


ssh-keygen -f "/home/witshine/.ssh/known_hosts" -R "172.16.167.165"


rancheros 持久化到硬盘
sudo ros c validate -i cloud-config.yml
sudo ros install -c cloud-config.yml -d /dev/sda

客户端Linux主机通过密钥远程登录
ssh -i ~/.ssh/id_rsa rancher@172.16.167.164

