# Python Posix Component

一些在 Unix & Linux 系统上编程的通用组件。

---

## 进程异常退出

https://sqlpy.com/blogs/143936893

有些时候我们会遇到服务端的进程异常退出了，针对这种情况就算有日志如果打的不对，也是不会被记录到日志文件的。

面对这种情况我们要有一个总的异常处理程序。

```python
from ppc.exceptions import catch_all

@catch_all("/tmp/err.log")
def main():
    """
    """
    ...
    pass
```

---