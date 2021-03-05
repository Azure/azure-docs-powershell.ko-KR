---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: ad4867bc97f35a6e027d0f944d936da1760d1033
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009131"
---
# Get-AzHDInsightMonitoring

## SYNOPSIS
클러스터에 대한 모니터링 설치 상태를 얻습니다.

## 구문

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzHDInsightMonitoring** cmdlet은 Azure HDInsight 클러스터에서 설치 모니터링 상태를 제공합니다. 모니터링을 사용하도록 설정하면 로그 분석 작업 영역 ID도 반환됩니다.

## 예제

### 예제 1
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

ClusterMonitoringEnabled 속성이 true이기 때문에 클러스터에서 모니터링이 활성화됩니다. 로그가 흐르는 모니터링 작업 영역 ID는 1d364e89-bb71-4503-aa3d-a23535aea7bd입니다.

### 예제 2
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

ClusterMonitoringEnabled 속성이 true이기 때문에 클러스터에서 모니터링이 활성화됩니다. 로그가 흐르는 모니터링 작업 영역 ID는 1d364e89-bb71-4503-aa3d-a23535aea7bd입니다.

### 예제 3
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

ClusterMonitoringEnabled 속성이 false이기 때문에 클러스터에서 모니터링을 사용하지 않도록 설정됩니다.

### 예제 4
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

ClusterMonitoringEnabled 속성이 false이기 때문에 클러스터에서 모니터링을 사용하지 않도록 설정됩니다.

## 매개 변수

### -DefaultProfile
azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
모니터링 상태를 얻을 클러스터의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
클러스터의 리소스 그룹입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring

## 참고 사항

## 관련 링크
