### 首页安装完成进行安全初始化操作
```
mysql_secure_installation
```
初始化操作主要用于：设置root密码；删除匿名账户；设置root管理员账户的远程登录操作；删除测试数据库test；刷新权限表

### 用户登录操作
```
mysql -u username -p
```

### 创建用户
```
create user username@host identified by 'password';
```

### 授权
```
grant select,update,delete,insert on database.table to username@localhost;
```

### 撤权
```
revoke select,update,delete,insert on database.table from username@localhost;
```

### 授权、撤权规范
| 命令        | 作用           |
| ------------- |:-------------:| 
| GRANT 权限 ON 数据库.表单名称 TO 用户名@主机名      | 对某个特定数据库中的特定表单给予授权 | 
| RANT 权限 ON 数据库.* TO 用户名@主机名     | 对某个特定数据库中的所有表单给予授权      | 
| GRANT 权限 ON *.* TO 用户名@主机名 | 对所有数据库及所有表单给予授权      |  
| GRANT 权限1,权限2 ON 数据库.* TO 用户名@主机名 | 对某个数据库中的所有表单给予多个授权      |  
| GRANT ALL PRIVILEGES ON *.* TO 用户名@主机名 | 对所有数据库及所有表单给予全部授权，（谨慎操作）      |  

### 查看某个用户的权限
```
show grants for username@localhost;
```
### 开启远程访问
```
grant all privileges on *.* to 'root'@'%' identified by 'root' with grant option;
```
