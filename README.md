> ###### 说明

* 操作系统CentOS 7
* 未使用TLS证书
* 执行安装前请修改hosts文件
* k8s基于v1.8.9
* 网络组件flannel
* 请修改roles/k8s-dns/files/kubedns-deployment.yaml文件中对应的master节点ip
* 由于相关的二进制安装包过大，请至https://dl.k8s.io/v1.8.9/kubernetes-server-linux-amd64.tar.gz 下载并解压
    * 将server/bin目录下的kube-apiserver、kube-controller-manager、kube-scheduler、kubectl 拷贝至 roles/k8s-master/files/目录下
    * 将server/bin目录下的kubelet、kube-proxy 拷贝至 roles/k8s-node/files/目录下

----

> ###### 安装命令

```
ansible-play site.yml -i hosts
```
