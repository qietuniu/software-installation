# redis在mac的安装与配置

## 安装

1. 官网下载：https://redis.io/download
2. 解压放在/usr/local 文件中（快捷键command+shift+G，输入/usr/local），解压文件命名为redis
3. 切换到redis文件夹 `cd /usr/local/redis/`
4. 编译测试 `sudo make test`
5. 编译安装 `sudo make install`
6. 服务器启动：`redis-server`

## 配置

1. 在/usr/local/redis查找redis.conf文件，打开进行编辑。（需要权限打开：系统偏好设置->安全与隐私->允许从以下位置下载应用->输入mac密码）
2. 修改密码： 文件内有 `# requirepass password` 可以直接查找password来定位，改成 `requirepass 123456`，即设置来123456的密码
3. 需要更改服务器地址的全局搜索`127.0.0.1`进行修改，默认主机的话不用修改
4. 在redis文件中执行 `redis-server redis.conf`


##  使用

- 设置：`SET KEY_NAME VALUE`
- 获取：`GET KEY_NAME`
- 停止服务：`redis-cli shutdown`


##  相关资源

- [Redis 官网](https://redis.io/)
- [Redis 在线测试](http://try.redis.io/)
- [菜鸟教程](https://www.runoob.com/redis/redis-tutorial.html)
