# Original Code

https://github.com/jhao104/proxy_pool

# Usage

1. download and upload the code

```bash
https://github.com/jhao104/proxy_pool/releases 下载对应zip文件
```

2. change the path and install the requirments

```bash
pip install -r requirements.txt
```

3. set the basic infomation

It seemend that the HOST should not be changed,and the PORT need to be opened.

```python
# setting.py 为项目配置文件

# 配置API服务

HOST = "0.0.0.0"               # IP
PORT = 5000                    # 监听端口


# 配置数据库

DB_CONN = 'redis://:pwd@127.0.0.1:8888/0'


# 配置 ProxyFetcher

PROXY_FETCHER = [
    "freeProxy01",      # 这里是启用的代理抓取方法名，所有fetch方法位于fetcher/proxyFetcher.py
    "freeProxy02",
    # ....
]
```

4. start it

```bash
# 如果已经具备运行条件, 可用通过proxyPool.py启动。
# 程序分为: schedule 调度程序 和 server Api服务

# 启动调度程序
python proxyPool.py schedule

# 启动webApi服务
python proxyPool.py server

```


5. visit it at `http://ip:port`

