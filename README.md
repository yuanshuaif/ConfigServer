该服务演示SpringCould的配置管理：
1.config server
    1.1 导包
    1.2 添加注解@EnableConfigServer
    1.3 在配置文件中配置相关配置
        配置git仓库的地址，以及配置文件的位置
        
2.bus
    2.1导包
    2.2配置文件中添加rabbitmq的信息
    2.3添加配置spring.cloud.bus.trace.enabled=true
    2.4暴露端点management.endpoints.web.exposure.include=bus-refresh
    2.5向config server发送 /bus-refresh的POST请求就可以
    
