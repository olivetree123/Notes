## Gunicorn Critical Error: WORKER TIMEOUT

### 现象
```
[CRITICAL] WORKER TIMEOUT (pid:25913)
[INFO] worker received SIGABRT signal
[INFO] Worker exiting (pid: 25913)
```

### 问题原因
目前问题原因并不明确，猜测是因为程序中有请求其他服务，但是该服务长时间未返回导致 Worker timeout。
Gunicorn 有个 timeout 参数，表示如果 Worker 进程在一定时间内未响应 Master 进程，则该 Worker 进程会被 kill 掉。

> timeout - If a worker does not notify the master process in this number of seconds it is killed and a new worker is spawned to replace it.

### 解决方案
解决方向主要有两个，一是增加 timeout 时长，二是使用异步 server， eventlet/gevent
1. [How to resolve the gunicorn critical worker timeout error?](https://serverfault.com/questions/490101/how-to-resolve-the-gunicorn-critical-worker-timeout-error?rq=1)
2. [Gunicorn CRITICAL WORKER TIMEOUT](https://github.com/benoitc/gunicorn/issues/1440)