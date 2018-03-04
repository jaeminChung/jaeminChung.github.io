---
layout: post
title:  "linux install java"
date:   2018-03-04
categories: linux
permalink: /archivers/linux-install-java
---

1. Download jdk from http://www.oracle.com/technetwork/java/javase/downloads/index.html
2. Move jdk file to /opt/.src
3. Extract file
```bash
 $ tar xvzf jdk-7u80-linux-x64.tar.gz
 $ tar xvzf jdk-8u121-linux-x64.tar.gz
```
4. Move jdk directory to /opt
```bash
 $ mv /opt/.src/jdk1.* /opt
```
5. Create symbolic link
```bash
 $ ln -s /opt/jdk1.8.0_121 /opt/java8
 $ ln -s /opt/jdk1.7.0.80  /opt/java7
 $ ln -s /opt/java8        /opt/java
```
6. Update alternatives
```bash
 $ sudo update-alternatives --install /usr/bin/java java /opt/java/bin/java 1
 $ sudo update-alternatives --install /usr/bin/javac javac /opt/java/bin/javac 1
 $ sudo update-alternatives --install /usr/bin/javaws javaws /opt/java/bin/javawa 1
```
7. Set java home
```bash
 $ sudo vi /etc/profile.d/java.sh
export JAVA_HOME=/opt/java
 $ source /etc/profile.d/java.sh
 $ echo $JAVA_HOME
```
