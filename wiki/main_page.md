---
redirect_from: /
published: true
---

# Welcome to my wiki page!

通过我的wiki，记录我完整的知识体系！

## Cloud Native

### kubernetes

Kubernetes 是一个可移植的、可扩展的开源平台，用于管理容器化的工作负载和服务，可促进声明式配置和自动化。Kubernetes 拥有一个庞大且快速增长的生态系统。Kubernetes 的服务、支持和工具广泛可用。

名称 **Kubernetes** 源于希腊语，意为 "舵手" 或 "飞行员"

Kubernetes 是什么？

https://kubernetes.io/zh/docs/concepts/overview/what-is-kubernetes/

##### [command](kubernetes_command.md)

##### docs

- [https://kubernetes.io/zh/docs/home/](https://kubernetes.io/zh/docs/home/)

##### blogs

- https://devopscube.com/install-configure-helm-kubernetes/
- [https://www.infoq.cn/article/KNMAVdo3jXs3qPKqTZBw](https://www.infoq.cn/article/KNMAVdo3jXs3qPKqTZBw)
- 

##### ebooks

- https://jimmysong.io/kubernetes-handbook/
- 

### Docker

**Docker** 最初是 `dotCloud` 公司创始人 [Solomon Hykes](https://github.com/shykes) 在法国期间发起的一个公司内部项目，它是基于 `dotCloud` 公司多年云服务技术的一次革新，并于 [2013 年 3 月以 Apache 2.0 授权协议开源](https://en.wikipedia.org/wiki/Docker_)，主要项目代码在 [GitHub](https://github.com/moby/moby) 上进行维护。`Docker` 项目后来还加入了 Linux 基金会，并成立推动 [开放容器联盟（OCI）](https://opencontainers.org/)。

**Docker** 自开源后受到广泛的关注和讨论，至今其 [GitHub 项目](https://github.com/moby/moby) 已经超过 5 万 4 千个星标和一万多个 `fork`。甚至由于 `Docker` 项目的火爆，在 `2013` 年底，[dotCloud 公司决定改名为 Docker](https://www.docker.com/blog/dotcloud-is-becoming-docker-inc/)。`Docker` 最初是在 `Ubuntu 12.04` 上开发实现的；`Red Hat` 则从 `RHEL 6.5` 开始对 `Docker` 进行支持；`Google` 也在其 `PaaS` 产品中广泛应用 `Docker`。

**Docker** 使用 `Google` 公司推出的 [Go 语言](https://golang.org/) 进行开发实现，基于 `Linux` 内核的 [cgroup](https://zh.wikipedia.org/wiki/Cgroups)，[namespace](https://en.wikipedia.org/wiki/Linux_namespaces)，以及 [OverlayFS](https://docs.docker.com/storage/storagedriver/overlayfs-driver/) 类的 [Union FS](https://en.wikipedia.org/wiki/Union_mount) 等技术，对进程进行封装隔离，属于 [操作系统层面的虚拟化技术](https://en.wikipedia.org/wiki/Operating-system-level_virtualization)。由于隔离的进程独立于宿主和其它的隔离的进程，因此也称其为容器。最初实现是基于 [LXC](https://linuxcontainers.org/lxc/introduction/)，从 0.7 版本以后开始去除 `LXC`，转而使用自行开发的 [libcontainer](https://github.com/docker/libcontainer)，从 1.11 开始，则进一步演进为使用 [runC](https://github.com/opencontainers/runc) 和 [containerd](https://github.com/containerd/containerd)。

##### [command](docker_commands.md)

##### docs

- https://docs.docker.com/

##### blogs

- https://draveness.me/docker/
- https://cizixs.com/2017/08/25/linux-cgroup/
- https://cizixs.com/2017/08/29/linux-namespace/

##### ebooks

- https://yeasy.gitbook.io/docker_practice/

#### Helm

做为Kubernetes的一个包管理工具，Helm具有如下功能：

- 创建新的chart
- chart打包成tgz格式
- 上传chart到chart仓库或从仓库中下载chart
- 在Kubernetes集群中安装或卸载chart
- 管理用Helm安装的chart的发布周期


Helm有三个重要概念：

1. chart：包含了创建Kubernetes的一个应用实例的必要信息
2. config：包含了应用发布配置信息
3. release：是一个chart及其配置的一个运行实例

##### command

##### docs

- [https://helm.sh/docs/](https://helm.sh/docs/)
- https://whmzsu.github.io/helm-doc-zh-cn/

##### blogs

##### key words

 [Go template language](https://godoc.org/text/template), 

## Linux tools

### [git](git.md)

### [vim](vim.md)

### [gdb](gdb.md)

curl

netstat

valgrind

ps

systemd

openssl

find

