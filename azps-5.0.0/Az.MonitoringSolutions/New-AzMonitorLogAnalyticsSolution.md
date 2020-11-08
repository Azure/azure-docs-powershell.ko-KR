---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 6747a53f9e714926c5a4d1358e15cb387ddae69a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226123"
---
# New-AzMonitorLogAnalyticsSolution

## SYNOPSIS
로그 분석 솔루션을 만듭니다.

## 구문과

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 설명은
로그 분석 솔루션을 만듭니다.

## 예제의

### 예제 1: 로그 분석 작업 영역에 대 한 모니터 로그 분석 솔루션 만들기
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

이 명령은 로그 분석 작업 영역에 대 한 모니터 로그 분석 솔루션을 만듭니다.

일반적으로 사용 되는 형식은 다음과 같습니다.

| 입력할 | 설명은 |
| :-----| :----- |
| Security센터 무료 |  Azure 보안 센터 – 무료 에디션 |
| 보안이 | Azure 보안 센터 |
| 업데이트 | 업데이트 관리 |
| ContainerInsights | 컨테이너에 대 한 Azure 모니터 |
| ServiceMap%) | 서비스 지도 |
| AzureActivity | 활동 로그 분석 |
| ChangeTracking | 변경 내용 추적 및 재고 |
| VMInsights | Vm 용 Azure 모니터 |
| SecurityInsights | Azure 센티널 |
| 네트워크 모니터링 | 네트워크 성능 모니터 |
| SQLVulnerabilityAssessment | SQL 취약점 평가 |
| SQLAdvancedThreatProtection | SQL 고급 위협 방지 |
| 방지 | 맬웨어 방지 평가 |
| AzureAutomation | 자동화 하이브리드 작업자 |
| LogicAppsManagement | 논리 앱 관리 |
| SQLDataClassification | SQL 데이터 검색 & 분류 |

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -위치
리소스 위치입니다.
로그 분석 작업 영역과 동일 해야 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
가져올 리소스 그룹의 이름입니다.
이름은 대/소문자를 구분 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.
구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### 태그
리소스 태그

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
만들려는 솔루션의 유형입니다.
예를 들어 "컨테이너".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceResourceId
솔루션이 배포/활성화 될 작업 영역의 Azure 리소스 ID입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

## 출력

### MonitoringSolutions. Api20151101Preview. ISolution에 대 한

## 상속자

별칭과

## 관련 링크



[Get-AzOperationalInsightsWorkspace](https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

