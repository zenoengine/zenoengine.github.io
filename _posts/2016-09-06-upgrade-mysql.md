---
layout: post
title: MYSQL 최신 버전 설치 / 업그레이드 하는 방법
description: ubuntu에서 mysql의 구버전을 신버전으로 업그레이드하면서 겪은 일을 정리했습니다. (5.5 -> 5.7)
tags :
  - mysql
  - ubuntu
---

MYSQL 최신 버전 설치 / 업그레이드 하는 방법

예: Mysql upgrade 5.5 to 5.7

# 1. MYSQL APT Repository 추가하기

mysql apt repository(url)[http://dev.mysql.com/downloads/repo/apt/]에서 다운로드합니다.

다운받는 링크주소를 확인한 후 wget으로 패키지를 받고 압축을 풉니다.

예시
```bash
$ wget http://dev.mysql.com/get/mysql-apt-config_0.7.3-1_all.deb
$ sudo dpkg -i mysql-apt-config_0.7.3-1_all.deb
```

그런 다음 패키지 정보를 업데이트 합니다.

```bash
$ sudo apt-get update
```

# 2. APT로 Mysql 설치

처음 설치라면

```bash
$ sudo apt-get install mysql-server 
```

기존 sql이 있다면

```bash
$ sudo apt-get upgrade mysql-server
```

# 3. MySQL 시작과 중지

mysql 상태 체크

```bash
$ sudo service mysql status
```

mysql 중지

```bash
$ sudo service mysql stop
```

mysql 시작

```bash
$ sudo service mysql start
```

# 주 버전 선택

```bash
$ sudo dpkg-reconfigure mysql-apt-config
```