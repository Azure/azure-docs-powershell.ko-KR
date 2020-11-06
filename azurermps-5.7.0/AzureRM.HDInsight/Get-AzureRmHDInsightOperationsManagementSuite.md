---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 38c7bfe31faa8b4f167a14ede75f92055919ba55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537752"
---
# Get-AzureRmHDInsightOperationsManagementSuite

## SYNOPSIS
클러스터의 OMS (Operations Management Suite) 설치 상태를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmHDInsightOperationsManagementSuite** Cmdlet은 Azure HDInsight 클러스터에서 OMS 설치의 상태를 가져옵니다. OMS를 사용 하는 경우에는 OMS 작업 영역 id도 반환 됩니다.

## 예제의

### 예제 1
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

ClusterMonitoringEnabled 속성이 true 이기 때문에 OMS (Operations Management Suite)가 클러스터에서 사용 하도록 설정 됩니다. 로그가 흐르는 OMS 작업 영역 id가 1d364e89-bb71-4503-aa3d-a23535aea7bd

### 예제 2
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

ClusterMonitoringEnabled 속성이 true 이기 때문에 OMS (Operations Management Suite)가 클러스터에서 사용 하도록 설정 됩니다. 로그가 흐르는 OMS 작업 영역 id가 1d364e89-bb71-4503-aa3d-a23535aea7bd

### 예제 3
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

ClusterMonitoringEnabled 속성이 false 이기 때문에 OMS (Operations Management Suite)는 클러스터에서 사용할 수 없습니다.

### 예제 4
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

ClusterMonitoringEnabled 속성이 false 이기 때문에 OMS (Operations Management Suite)는 클러스터에서 사용할 수 없습니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
OMS (Operations Management Suite) 상태를 가져올 클러스터의 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
클러스터의 리소스 그룹입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### AzureHDInsightOMS를 통해 관리 합니다.

## 상속자

## 관련 링크

