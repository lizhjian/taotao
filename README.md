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
   