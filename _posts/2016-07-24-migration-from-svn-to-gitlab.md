---
layout: post
title: SVN-Git GitLab 마이그레이션
description: SVN 저장소에서 GitLab 저장소로 마이그레이션하는 방법입니다.
tags :
  - git
  - gitlab
---

최근 개인 저장소로 유용하게 쓰고있던 네이버 svn 프로젝트가 폐쇠된다는 소식을 듣고 git 로 마이그레이션을 결정 했습니다.

속도, 여러명의 사람 가입, 바이너리 지원 잘되는 무료 git 저장소 서비스를 찾다보니 gitlab 이 가장 적절하다는 결론을 냈습니다.

이에 옮기는 과정을 가장 쉬운 방법으로 간단한 포스팅 하려 합니다.

### 1. svn 히스토리를 git 로 가져오기

```php
git svn clone <svn주소> -s
```

위의 커맨드는 기존 svn에서 관리하던 코드들을 git 표준으로 가져옵니다.

### 2. gitlab 저장소 생성

우선 GitLab 사이트에 가서 접속을 하고 New Project를 통해 새 저장소를 생성합니다.

### 3. SourceTree 사용

git clinet인 SourceTree를 설치합니다.

File-Open 을 통해 1번에서 생성한 디렉토리를 선택하여 북마크에 추가합니다.

그 후 svn 프로젝트를 선택하고 Setting-Remotes-Add-(2번에서 생성한 새 프로젝트 주소<ex) https://gitlab.com/*.git> )

### 4.Push 후 확인

Push를 하고 웹사이트에서 본인의 프로젝트에 코드들이 Push 됬는지 확인합니다.