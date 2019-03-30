引入运行环境
## FROM  hub.c.163.com/library/java:8-alpine


写入作者信息
## MAINTAINER tieminPan 1255070026@qq.com


添加jar包并并重命名
## ADD  target/*.jar app.jar

端口
## EXPOSE 8761


运行命令
## ENTRYPOINT ["java","-jar","/app.jar"]


构建docker文件
## build -t 文件名:版本 路径
如:
## build -t springcloud_eureka:0.2 .


设置仓库远程地址以及标签
## docker tag springcloud_eureka:0.2  reg.qiniu.com/tmpan-cn/springcloud_eureka:0.2


推送到远程容器仓库
## docker push reg.qiniu.com/tmpan-cn/springcloud_eureka:0.2
