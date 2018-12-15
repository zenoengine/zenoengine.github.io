---
layout: post
title: CentOS minimal 설치 후 Network 설정
description: CentOS 최소 설치를 하면 인터넷이 되지 않습니다. 인터넷을 사용하기위해 Network 설정하는 법을 정리했습니다.
share: true
comments: true
tags:
  - centos
  - linux
---

CentOS minimal 설치 직후 network 설정을 해줘야 인터넷을 통해 패키지 설치나 다운로드가 가능해집니다.


### 방법 1 cmmand line 

```js
vi /etc/sysconfig/network-scripts/ifcfg-enp0s3
```

```
ONBOOT = yes로
```

네트워크 서비스 재시작

```
service network restart
```

### 방법 2 TUI

```
nmtui
```

Edit Connection - Automatically connection

에서 spacebar 를 누르면 자동 연결설정을해줍니다.


네트워크 서비스 재시작

```
service network restart
```