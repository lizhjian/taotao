基于分布式的商城项目
##第一课
###搭建工程
* taotao
  * taotao-parent父工程，打包当时为pom管理jar包版本号所有工程都继承该工程
   * taotao-common  通用的工具类 打包方式jar
   * taotao-manager 服务层工程，聚合工程 pom工程 
     * taotao-manager-dao  打包方式jar
     * taotao-manager-pojo 打包方式jar
     * taotao-manager-interface 打包方式jar
     * taotao-manager-service  打包方式war
   * taotao-manager-web  打包方式war
  
###dubbo 
  远程通信方式
  * Webservice:效率不高 基于soap协议，项目中不推荐使用
  * 使用restful形式的服务：http+json 如果服务太多吗，服务之间调用关系混乱 
  * web 和service是两个单独的工程，通过dubbo进行通信，使用rpc协议进行远程调动，直接使用socket
   通信。传输效率高，并且可以统计出系统之间的调用关系、调用次数 
   1、container2、Registry 3、Consumer4、Monitor 5、Provider 
   * container --start-----> provider  容器启动提供者
   * provider -- register--> Registry  到注册中心注册
   * Consumer -- subscribe--> Registry  消费者找中介公司订阅
   * Registry -- notify--> Consumer  中介公司通知消费者
   * Consumer -- invoke--> Provider  顾客找到提供者
   * Consumer+Provider ---count---> Monitor  生产者消费者都被监控中心监控
   2.
   