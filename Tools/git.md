# configure ssh

ssh-keygen: 用来生成ssh公钥认证所需的公钥和私钥文件, 可用于github项目管理时免密通信。

```bash
ssh-keygen
cat ~/.ssh/id_rsa.pub # 将此复制到github
```

add your email and username


```bash
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```

# 代理

Git目前支持的三种协议 `git://、ssh:// 和 http://`

其代理配置各不相同：

    - core.gitproxy 用于 git:// 协议，
    - http.proxy 用于 http:// 协议，
    - ssh:// 协议的代理需要配置 ssh 的 ProxyCommand 参数

```bash
git config --global https.proxy http://127.0.0.1:10800
git config --global https.proxy 'socks5://127.0.0.1:10800'
git config --global core.gitproxy <run proxy script>
git config --global --unset http.proxy]
```
