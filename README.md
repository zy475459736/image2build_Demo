# Java应用容器化的案例
## 方式

目前整理了三种将 Java应用制作成Docker镜像的方式。

* DockerFile + Docker Daemon
* plugin spotify
* plugin jib

## 基础镜像
* fabric8/java-jboss-openjdk8-jdk
* openjdk:8-jdk-alpine
* gcr.io/distroless/java

## Multistage