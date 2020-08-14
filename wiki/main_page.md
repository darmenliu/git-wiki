---
redirect_from: /
published: true
---

# Welcome to my wiki page!

通过我的wiki，记录我完整的知识体系！

## Cloud compute

Cloud computing is a type of Internet-based computing that provides shared computer processing resources and data to computers and other devices on demand. It is a model for enabling ubiquitous, on-demand access to a shared pool of configurable computing resources (e.g., computer networks, servers, storage, applications and services),[1][2] which can be rapidly provisioned and released with minimal management effort. Cloud computing and storage solutions provide users and enterprises with various capabilities to store and process their data in third-party data centers[3] that may be located far from the user–ranging in distance from across a city to across the world. Cloud computing relies on sharing of resources to achieve coherence and economy of scale, similar to a utility (like the electricity grid) over an electricity network.

### Virtualization（虚拟化）

- Virtualization is a technique that allows running more than one server with its operation system (i.e. Virtual Machines) on the same hardware.
- Virtualization abstracts the hardware layer from the software layer
- Virtualization allows server consolidation, which results in HW utilization efficiency improvement
- Virtual Machine provides the runtime environment for the Guest OS and Guest Applications 
- Hypervisor (VMware ESXi, KVM) is responsible for emulating hardware configurations to Guest OS
- Host OS provides the boot environment for the hypervisor (if bare-metal hypervisor is not used)

#### 虚拟化类型

1. 全虚拟化（Full Virtualization）

   全虚拟化是指虚拟机模拟了完整的底层硬件，包括处理器、物理内存、时钟、外设等，使得为原始硬件设计的操作系统或其它系统软件完全不做任何修改就可以在虚拟机中运行。比较著名的全虚拟化 VMM 有 Microsoft Virtual PC、VMware Workstation、Sun Virtual Box、Parallels Desktop for Mac 和 QEMU。

2. 超虚拟化（Paravirtualization）

   这是一种修改 Guest OS 部分访问特权状态的代码以便直接与 VMM 交互的技术。在超虚拟化虚拟机中，部分硬件接口以软件的形式提供给客户机操作系统。比较著名的 VMM 有 Denali、Xen。

3. 硬件辅助虚拟化（Hardware-Assisted Virtualization）

   硬件辅助虚拟化是指借助硬件（主要是主机处理器）的支持来实现高效的全虚拟化。例如有了 Intel-VT 技术的支持，Guest OS 和 VMM 的执行环境自动地完全隔离开来，Guest OS 有自己的“全套寄存器”，可以直接运行在最高级别。Kvm属于该种类型。

4. 部分虚拟化（Partial Virtualization）

   VMM 只模拟部分底层硬件，因此客户机操作系统不做修改是无法在虚拟机中运行的，其它程序可能也需要进行修改。在历史上，部分虚拟化是通往全虚拟化道路上的重要里程碑，最早出现在第一代的分时系统 CTSS 和 IBM M44/44X 实验性的分页系统中。

5. 操作系统级虚拟化（Operating System Level Virtualization）

   操作系统级虚拟化是一种在服务器操作系统中使用的轻量级的虚拟化技术，内核通过创建多个虚拟的操作系统实例（内核和库）来隔离不同的进程，不同实例中的进程完全不了解对方的存在。比较著名的有 Solaris Container FreeBSD Jail 和 OpenVZ 等。

VM

KVM（Kernel-based Virtual Machine）

Xen

Open vSwith

DPDK

### NFV（Network Function Virtualization）

VNF

VNFC



## Cloud Native

### kubernetes

Kubernetes 是一个可移植的、可扩展的开源平台，用于管理容器化的工作负载和服务，可促进声明式配置和自动化。Kubernetes 拥有一个庞大且快速增长的生态系统。Kubernetes 的服务、支持和工具广泛可用。

名称 **Kubernetes** 源于希腊语，意为 "舵手" 或 "飞行员"

Kubernetes 是什么？

https://kubernetes.io/zh/docs/concepts/overview/what-is-kubernetes/

##### [command](kubernetes_command.md)

##### docs

- [https://kubernetes.io/zh/docs/home/](https://kubernetes.io/zh/docs/home/)
- https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.18/

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

##### [command](helm_commands.md)

##### docs

- [https://helm.sh/docs/](https://helm.sh/docs/)
- https://whmzsu.github.io/helm-doc-zh-cn/

##### blogs

##### key words

 [Go template language](https://godoc.org/text/template),  [Sprig template library](https://godoc.org/github.com/Masterminds/sprig), [SemVer 2](https://semver.org), YAML, 

## Linux tools

##### Useful docs

Linux工具快速教程: https://linuxtools-rst.readthedocs.io/zh_CN/latest/index.html#

##### blogs

##### key words

### [git](git.md)

Git 是一个开源的分布式版本控制系统，用于敏捷高效地处理任何或小或大的项目。

Git 是 Linus Torvalds 为了帮助管理 Linux 内核开发而开发的一个开放源码的版本控制软件。

Git 与常用的版本控制工具 CVS, Subversion 等不同，它采用了分布式版本库的方式，不必服务器端软件支持

### [vim](vim.md)

Linux 上比较强大的文本编辑器。

guide：[https://www.runoob.com/linux/linux-vim.html](https://www.runoob.com/linux/linux-vim.html)

### [gdb](gdb.md)

GDB是一个由GNU开源组织发布的、UNIX/LINUX操作系统下的、基于命令行的、功能强大的程序调试工具。 对于一名Linux下工作的c++程序员，gdb是必不可少的工具；

### [curl](curl.md)



### [netstat](netstat.md)



### [valgrind](valgrind.md)



### [ps](ps.md)



### [systemd](systemd.md)



### [openssl](openssl.md)



### [find](find.md)



### [grep](grep.md)



### [httperf](httperf.md)



### [sed](sed.md)

