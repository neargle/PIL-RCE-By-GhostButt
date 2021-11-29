# Exploiting Python PIL Module Command Execution Vulnerability

攻击由 PIL 开发的 Python 应用, 并达到远程命令执行的效果。这个项目用来放paper和实验所用到的源码和Dockerfile。

Paper : https://github.com/neargle/PIL-RCE-By-GhostButt/blob/master/Exploiting-Python-PIL-Module-Command-Execution-Vulnerability.md

Vulhub: https://github.com/vulhub/vulhub/tree/master/python/PIL-CVE-2017-8291

## Install

```bash
git clone https://github.com/neargle/PIL-RCE-By-GhostButt.git && cd PIL-RCE-By-GhostButt
docker-compose build
docker-compose up -d
```

View http://localhost:8000/, upload poc.png.

More info : [paper.md](https://github.com/neargle/PIL-RCE-By-GhostButt/blob/master/Exploiting-Python-PIL-Module-Command-Execution-Vulnerability.md)
