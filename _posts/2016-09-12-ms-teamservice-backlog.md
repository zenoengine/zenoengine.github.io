---
layout: post
title: Visual studio Teamservice 활용하기 (1) - Agile Tool "BackLog"
description: Agile Tools 중 하나인 BackLog를 사용하는 방법에 대해 정리했습니다.
share: true
comments: true
tags :
  - microsoft
  - teamservice
  - agile
---
<style>
  .mbtablestyle {
    border-collapse: collapse;
  }
  
  td,
  th {
    border: 1px solid black;
    padding: 5px;
  }
</style>

MS Teamservice는 팀 개발에 필요한 좋은 툴과 코드 저장소를 제공하는 서비스입니다.

제가 생각하는 TeamService의 강점은 다음과 같습니다.

- 5인 이하에게 무료
- 저장소 무제한, 용량 무제한
- Visual studio와의 연동
- Azure와 연동
- Agile Tools **무료** 제공

5인 이하의 프로그래머로 구성된 스타트 업이나 학생들에게 추천드릴 수 있겠네요.

이 글에서는 Agile Tools 중 BackLog에 대해 살펴보도록 하겠습니다.

# BackLog

Product BackLog는 팀이 프로젝트를 계획하고 무엇을 만들어 제공할지에 대한 로드맵입니다. 

BackLog를 사용하면 프로젝트 관리에서 다음과 같은 이점을 얻을 수 있습니다.

```
- 기능 및 빌드 요구사항의 우선순위 목록을 관리
- 기록 추적 가능
- 팀 공유에 필요한 모든 정보 저장소 제공
```

그럼 BackLog를 사용하는 방법에 대해 살펴보겠습니다.

## - BackLog 열기


Visual studio Teamservice 화면에서 Wrok 영역에 있는 BackLog를 눌러 접근할수 있습니다.

![BackLog Position](https://rzjxkw.by3301.livefilestore.com/y3mLMJRSyIjIlYRTsFzs-eAJHN_iRpNc6jiOWskYDl5wyKlEoARV34ramJ5EaPCvgqTdlDs9bL64vXsxL2N7o7O8caKJ1hkLNCzoy7oDIByfEHYWJ-JRiTZgoLbB5RBxXYvnNt_usw4EwFGGh_BRW9tuTn-x6AyoVLXOepy4ix_bQs?width=701&height=454&cropmode=none)

혹시 아직 Visual studio teamservice를 시작하지 않았다면 다음의 [페이지](https://azure.microsoft.com/ko-kr/services/visual-studio-team-services/)에서 시작할 수 있습니다.

## - BackLog 구축

모든 주제들에 대해 제목을 입력하고 Add 버튼을 눌러 항목을 추가합니다.

![Build BackLog](https://rzlynw.by3301.livefilestore.com/y3mfq2kXtr0gWO86ZbP1-1WzkdJHeXZwfLWKEkFRuZsLvvhd6_pmaPr6Wtel3aKh8BM8QOWpJjm1S3Wg1HOlxSWu52DK2sG04rGFjl9lTgz5rLwdA2ETnSPD2C0mxE3braIos0nPVGANE6Hh88MMNrz8bAqK2QiL5z1uL3Ty06GS6c?width=634&height=299&cropmode=none)

만약 이미 작성해두었던 목록이 있다면 다시 칠 필요 없이 [microsoft excel](https://www.visualstudio.com/en-us/docs/work/office/bulk-add-modify-work-items-excel)을 이용해서 빠르게 BackLog로 가져올 수 있습니다.

## - 우선순위 변경

항목들을 BackLog에 추가했다면 우선순위를 조절 할 수 있습니다.

자주 우선 순위를 변경하고 재검토하는 것은, 여러분들의 팀이 해야할 가장 중요한일들을 알게 해줄 것입니다.

![priority order](https://i3-vso.sec.s-msft.com/en-us/docs/work/BackLogs/_img/alm_cb_orderBackLog.png)

## - 세부 사항과 견해 추가

BackLog를 구축하고 우선 순위를 정하는것은 추상적인 로드맵을 만들 수 있지만, 일을 시작하기전에 좀더 세부적인 사항이 필요할것입니다.

각 아이템들을 더블클릭하면 여러분은 다음과 같은 정보 수정 창을 찾을 수 있을겁니다.

각 정보를 적을 때 최대한 상세히 적어주는것이 좋습니다. 팀원들이 작업에 대한 이해, 공수 예측, 개발 테스팅, 제품 허용 만족기준을 산정하는데 도움이 되기 때문입니다.

![add detail](https://i3-vso.sec.s-msft.com/en-us/docs/work/BackLogs/_img/cyb-product-BackLog-form-ts.png)

세부 사항에 대한 자세한 사항은 [이곳](https://www.visualstudio.com/en-us/docs/work/BackLogs/add-work-items-tfs)에 있으며 핵심적인 요소 몇가지에 대해 짚고 넘어가겠습니다.

|항목|용도|
|---|---|
|Effort| 항목의 일을 끝내는데 들어가는 노력의 예측량입니다. |
|Business Value| 특별한 우선 순위인 "사업적 가치" 를 수량화 한 것입니다. 숫자가 높을수록 높은 사업적 가치를 지니며, 다른 항목과 상대적인 가치판단을 하는데 도움이 됩니다. (TFS 버전에서 해당)|
|Description| 만드는것에 대한 이해도를 높이고 공수 예측을 돕기위해 충분한 설명을 적어야합니다. 어떻게 개발하는가가 아닌 사용자가 원하는 것에 대해 초점을 맞추고 작성해야합니다. |
|Acceptance Criteria| "완료" 보고를 어느 시점, 기준을 통해 할것인지 설명합니다. |
{:.mbtablestyle}


# - 다중 항목 이동

다수의 항목을 다른 Sprint에 넣고 싶다면 Ctrl 혹은 Shift + click 을 통해 여러 항목을 선택후 다른 sprint 항목으로 드래그 드롭을 하거나, 

▼ 버튼을 눌러 이동한 sprint를 선택하는 것으로 가능합니다. 

![bulk move](https://i3-vso.sec.s-msft.com/en-us/docs/work/BackLogs/_img/BackLog-multi-select-non-sequential-items.png)

### ※Agile 상식 : Sprint란?

```
반복적인 개발 주기 (회사에서 정하는 이터레이션이 개발 주기가 된다. 계획 회의 부터 제품 리뷰가 진행 되는 날짜 까지의 기간이 1스프린트 이다)
```

대략 21~30 가량을 많이들 잡으며 Current iteration, Feauter iteration 등이 있겠네요.

이상 VisualStudio TeamService에서 제공해주는 BackLog에 대해 간단하게 살펴보았습니다!