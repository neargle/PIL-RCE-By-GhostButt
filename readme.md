# Exploiting Python PIL Module Command Execution Vulnerability

PIL (Python Image Library) 应该是 Python 图片处理库中运用最广泛的，它拥有强大的功能和简洁的API。很多Python Web应用在需要实现处理图片的功能时，都会选择使用PIL。

PIL在对 eps 图片格式进行处理的时候，如果环境内装有 GhostScript，则会调用 GhostScript 在dSAFER模式下处理图片，即使是最新版本的PIL模块，也会受到 `GhostButt CVE-2017-8291` dSAFER模式Bypass漏洞的影响，产生命令执行漏洞。

## 一个简单常见的Demo

```python
from PIL import Image
def get_img_size(filepath=""):
    '''获取图片长宽'''
    if filepath:
        img = Image.open(filepath)
        img.load()
        return img.size
    return (0, 0)
```
