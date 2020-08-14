# GDB

guide: https://linuxtools-rst.readthedocs.io/zh_CN/latest/tool/gdb.html



docker里面生成coredump时需要在宿主机里面修改内核参数
ulimit -c unlimited
echo 1 > /proc/sys/kernel/core_uses_pid
echo "/tmp/corefile-%e-%p-%t" > /proc/sys/kernel/core_pattern



多进程gdb调试时，使用如下命令设置断点是在父进程还是在子进程
set follow-fork-mode [parent|child]
• parent: fork之后继续调试父进程，子进程不受影响。
• child: fork之后调试子进程，父进程不受影响。



在docker里面使用gdb进行调试的话需要docker需要增加如下参数 --security-opt seccomp=unconfined
docker run  -p 192.168.99.100::22 -p 192.168.99.100::80 -ti -v //mnt/share:/mnt/share --name rcpdevenv --security-opt seccomp=unconfined ubuntu:latest /usr/sbin/sshd -D



layout：用于分割窗口，可以一边查看代码，一边测试。主要有以下几种用法：
layout src：显示源代码窗口
layout asm：显示汇编窗口
layout regs：显示源代码/汇编和寄存器窗口
layout split：显示源代码和汇编窗口
layout next：显示下一个layout
layout prev：显示上一个layout
Ctrl + L：刷新窗口
Ctrl + x，再按1：单窗口模式，显示一个窗口
Ctrl + x，再按2：双窗口模式，显示两个窗口
Ctrl + x，再按a：回到传统模式，即退出layout，回到执行layout之前的调试窗口。
设置gdb的代码目录
directory /home/src_code


gdb remote
server: gdbserver 10.106.229.155:9000 ./test
client : gdb : target remote 192.168.1.199:9000
login the vpn: https://10.68.148.38/dana-na/auth/url_default/welcome.cgi