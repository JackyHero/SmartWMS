一、项目简介：
     
    SmartWMS为了降低物流仓储企业的信息化成本，决定全面开源
    此产品。

    产品特点：
    1、适用范围：第三方物流仓储企业，冷链仓库，工厂仓储，海外仓等。
    2、技术特点：基于JAVA的WEB后台，基于UNI-APP开发的PDA系统。
    3、功能特点：涵盖订单管理系统（OMS），仓储管理系统（WMS），计费管理系统（BMS），现场作业系统（RF），第三方接口模块
    4、接口支持：已经对接：SAP ECC，SAP HANA 数据库，用友U8。
    5，AGV模拟程序：加入了基于PLC的模拟程序，大家可以基于此思路研究AGV的调度。
   

二、业务介绍：    

    1、主要功能
        计费配置、仓库配置、基础配置、计费管理、基础资料、仓库管理、月台管理、进货管理、出货管理、退货管理、库内管理、盘点管理、
        库存查询、PDA功能、分析报表、分析图表、域验证。
    2、主要流程
        客户下单流程，收货流程，上架流程，移货作业、拣货流程：批量拣货，按单拣货、盘点流程、计费流程。
    3、硬件对接
        对接自主研发基于LORA物联网技术的电子货架标签模块，满足快速退货分拣，波次拣货；对接自动化立体库系统，对接AGV，RFID。
    4、计费管理：通过在线SQL，动态完成费用的计算，满足3PL仓费用复杂多变的需求。

三、安装说明：
  
    1，开发环境：
       开发工具：
		IDEA（版本不限）；
		JDK1.8
		Maven
		Mysql5.7以上（注意设置大小写不敏感，关闭only_full_group_by规则  
               # 设置sql_mode，去掉了ONLY_FULL_GROUP_BY
               sql_mode='STRICT_TRANS_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO,NO_ENGINE_SUBSTITUTION'），mysql8.0不行
		运行环境：CENTOS6.5以上或windows server 2008、tomcat7以上，JDK1.8， MYSQL5.7
    2，按照mvn方式导入
    3，数据库还原：
        安装完数据库执行下 GRANT ALL PRIVILEGES ON *.* TO 'root'@'%'IDENTIFIED BY '你的密码' WITH GRANT OPTION;
                          FLUSH PRIVILEGES;     
        步骤 
        1：还原数据库，
        2:修改 dbconfig.properties
        3: sql导入方式建议 登录MYSQL服务器上用source命令还原,或用Mysqlworkbench importing
    4，IDEA：mvn tomcat7:run   输入用户名和密码：admin llg123
    5、主要技术
        开发语言：JAVA。
    6、技术架构
	基础架构基于jeecg。技术架构为SpringMVC+Hibernat+Minidao(类Mybatis)+Easyui(UI库)+ Jquery + Bootstrap + Ehcache + Redis + Ztree等基础架构
	
   
   


