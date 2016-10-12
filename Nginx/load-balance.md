### load balance
配置上游节点 upstream
```
upstream myserver {
  server src.exam.com;
  server src1.exam.com;
}
location / {
  proxy_pass http://myserver;
}
```
