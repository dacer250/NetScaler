# Citrix NetScaler 简介 入门介绍

附图 和 中文手册.足够

https://wenku.baidu.com/view/65707f130b4e767f5acfce46.html

官方手册: 内含API
https://docs.citrix.com/en-us/netscaler/11.html

# 对于负载均衡来说
 1.首先在NC上增加物理Server,配置services. 由于是做负载均衡,这种service肯定是多个的.例如:
    192.168.1.100:8080 -> http-login-8080
    192.168.1.200:9090 -> http-login-9090
    170.70.10.10:9090 -> http-service-170
   以上是三个相同的web应用,分别部署在三台物理服务器上.在NC配置后,形成3个services.
  2. 建立Virtual Server . 这个 Virtual Server 下面就有这三个service,通过配置权重来做负载均衡.
  
  由此可见. 一个VServer是 相同功能的Service的集合. 这个集合内部按照算法做负载均衡.

