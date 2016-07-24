---
layout: post
title: CentOS minimal 설치 후 Network 설정
---

CentOS minimal 설치 직후면 network 설정을 해줘야합니다.



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