# macOS firewall settings

### 获取 networksetup 所有配置
```bash
networksetup -help
```

### 设置 http 代理
```bash
networksetup -setwebproxy Wi-fi 127.0.0.1 8080
```

### 设置 http 代理状态 (打开/关闭)
```bash
# 打开
networksetup -setwebproxystate Wi-Fi on
networksetup -setwebproxystate Wi-Fi off
```

### 设置 https 代理
```bash
networksetup -setsecurewebproxy Wi-fi 127.0.0.1 8080
```

### 设置 https 代理状态 (打开/关闭)
```bash
# 打开
networksetup -setsecurewebproxystate Wi-Fi on
networksetup -setsecurewebproxystate Wi-Fi off
```


### 设置 socks 代理
```bash
networksetup -setsocksfirewallproxy Wi-Fi 127.0.0.1 7070
```

### 获取当前 socks 代理配置和状态
```bash
networksetup -getsocksfirewallproxy Wi-Fi
```

```
Enabled: Yes
Server: 127.0.0.1
Port: 7070
Authenticated Proxy Enabled: 0
```

### 设置 socks 代理状态 (打开/关闭)
```bash
networksetup -setsocksfirewallproxystate Wi-Fi on
networksetup -setsocksfirewallproxystate Wi-Fi off
```


# windows 设置
```bash
// 打开关闭 lan  1 | 0
reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyEnable /t REG_DWORD /d 1 /f
```

```bash
// 修改代理 ip
reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Internet Settings" /v ProxyServer /t REG_SZ /d 127.0.0.1:3388 /f
```

