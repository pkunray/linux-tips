## 端口转发:
ssh -L 2121:host2:21 host3
2121 为本地端口，host2 为目的主机，21 为目的端口，host3 为中间主机。
效果：通过 2121 端口的数据全部经由 host3 转发至 host2 主机的 21 端口。
如果没有 host3 上的 root 用户，办法如下：
ssh -L 2121:host2:21 user@host3

## 参考：
1.SSH原理与运用（一）：远程登录 http://www.ruanyifeng.com/blog/2011/12/ssh_remote_login.html
2.SSH原理与运用（二）：远程操作与端口转发 http://www.ruanyifeng.com/blog/2011/12/ssh_port_forwarding.html
