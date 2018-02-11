# nginxupstreamdemo

### 本机安装docker及docker-compose

在项目文件下启动nginx
```
sudo docker-compse up
```

springbootserver1、springbootserver2为两个springboot工程，可直接导入eclipse，或执行mvn clean package生成jar文件

启动两工程后，访问http://127.0.0.1:81/api/test,多次执行测试代理是否成功

nginx配置文件见conf.d目录下的两个文件，upstream.conf配置代理ip及端口，test.conf文件中proxy_pass http://springbootserver;指定了使用的先关配置
