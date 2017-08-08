### 作为windows服务
```
"C:\Program Files\MongoDB\Server\3.4\bin\mongod.exe" --config "e:\data\mongodb\mongod.conf" --install
net start MongoDB
net stop MongoDB
"C:\Program Files\MongoDB\Server\3.4\bin\mongod.exe" --remove
```
