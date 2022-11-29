项目介绍
架构
JDK 1.8
springboot 2.3.2.RELEASE
mybatis plus 3.4.2
alibaba druid 连接池
服务
结算审计模块 -> flyedt-qddt-jssj
公共部分 -> flyedt-qddt-common
开发说明
工具类与库
以下工具类与库已经引入，请大家根据业务选用，勿重复引包、勿重复封装
pom.xml请勿随意引入依赖，需要引入依赖包是要说一下，以防版本冲突、重复依赖等各种问题
mybatis plus
// <dependency>
//     <groupId>com.flyedt</groupId>
//     <artifactId>flyedt-mybatis-plus</artifactId>
// </dependency>

// 已集成MybatisPlusInterceptor分页插件
// 实体类请继承：com.flyedt.utils.mybatisplus.BaseEntity
// interface mapper请继承：com.baomidou.mybatisplus.core.mapper.BaseMapper
// interface service请继承：com.flyedt.utils.mybatisplus.BaseService
// class service请继承：com.flyedt.utils.mybatisplus.BaseServiceImpl
系统认证用户
// 获取当前认证用户信息：com.flyedt.utils.web.UsersUtils
系统访问IP
// 获取访问IP：com.flyedt.utils.web.UsersUtils.getIp()
commons
// commons-lang3 -> 字符串工具类、对象工具类、随机字符串和数值工具类、系统工具类、数值工具类、数组工具类、布尔工具类……
// commons-collections4 -> 集合工具库
// commons-codec -> 编解码库
// commons-io -> FileUtils、IOUtils、FilenameUtils……
fastjson
// fastjson -> JSON库
localDate和localDateTime工具类
// com.flyedt.commons.utils.LocalDateUtils
http
// 发送http请求/执行Http方法请使用：com.flyedt.commons.httpclient.HttpClientUtils
雪花算法id生成器
// com.flyedt.commons.snowflake.SnowflakeIdWorker
// 方法：SnowflakeIdWorker.generateId()
oss对象存储、文件相关操作
// <dependency>
//     <groupId>com.flyedt</groupId>
//     <artifactId>flyedt-oss</artifactId>
// </dependency>

// 附件表service：com.flyedt.oss.service.AttachService
// 业务附件表service：com.flyedt.oss.service.BizAttachService

// 文件上传：com.flyedt.oss.utils.file.FileUploadUtils
// 从网络地址下载文件：com.flyedt.commons.file.FileDownloadUtils
自定义异常
// 自定义异常请继承：com.flyedt.commons.exception.SystemException
加解密
// com.flyedt.commons.utils.RSAEncryptUtils
// com.flyedt.commons.utils.Md5Utils
// com.flyedt.commons.utils.AesUtils
poi-tl
// Word模板引擎，通过占位符替换docx文件中的文本、图片、表格、列表、图表、样式等
// com.flyedt.common.utils.PoiTiExample
FTP
// com.flyedt.commons.ftp.FTPSClientUtils
webservice
// com.flyedt.commons.webservice.Axis2InvokeWebservice
// com.flyedt.commons.webservice.AxisInvokeWebservice
// com.flyedt.commons.webservice.HttpInvokeWebservice
activiti工作流
// <dependency>
//     <groupId>com.flyedt</groupId>
//     <artifactId>flyedt-activiti</artifactId>
// </dependency>

// 模型service：com.flyedt.workflow.service.ModelBusinessService
// 流程service：com.flyedt.workflow.service.ProcessDefinitionService
// 实例service：com.flyedt.workflow.service.ProcessInstanceService
// 任务service：com.flyedt.workflow.service.TaskBusinessService
开发规约
包结构说明
// config：过滤器、拦截器、自定义异常、自动装配等各类配置
// constant：常量、自定义属性或从配置文件读取的属性……
// controller：视图层
// service：业务层
// mapper：持久层
// entity：实体
// dto：入参
// vo：返参
// enums：枚举
// api：与第三方系统交互
// feign：服务之间通讯工具openfeign
// annotation：自定义注解
// aspect：切面
// utils：工具
// ……
编码规范
/**
* 1. 入参请定义DTO，返参请定义VO，实体类禁止向外部暴露
* 2. 采⽤4个空格缩进
* 3. IDE的text file encoding设置为UTF-8
* 4. 缩⼩变量的作⽤域
* 5. 复杂的业务必须写在service层，并且加备注
* 6. 事务必须写到service层，禁止写到controller
* 7. ⾦额运算使⽤BigDecimal
* 8. 使⽤log打印⽇志
* 9. 不用或少用魔法值，可选用定义枚举、定义常量、定义属性的方式
     */

编码规范
/**
* 1. 入参请定义DTO，返参请定义VO，实体类禁止向外部暴露
* 2. 采⽤4个空格缩进
* 3. IDE的text file encoding设置为UTF-8
* 4. 缩⼩变量的作⽤域
* 5. 复杂的业务必须写在service层，并且加备注
* 6. 事务必须写到service层，禁止写到controller
* 7. ⾦额运算使⽤BigDecimal
* 8. 使⽤log打印⽇志
* 9. 不用或少用魔法值，可选用定义枚举、定义常量、定义属性的方式
     */