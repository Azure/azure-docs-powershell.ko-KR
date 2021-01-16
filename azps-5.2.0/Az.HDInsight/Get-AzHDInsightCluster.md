---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: 289f7b4bf397384b1420af02a5517e57bf51675d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326745"
---
# Get-AzHDInsightCluster

## SYNOPSIS
현재 구독 또는 지정된 리소스 그룹과 연결된 모든 Azure HDInsight 클러스터를 가져온 후 나열하거나 특정 클러스터를 검색합니다.

## 구문

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzHDInsightCluster** cmdlet은 현재 구독에 대한 Azure HDInsight 서비스 클러스터를 나열합니다.
*ClusterName* 매개 변수를 사용하여 특정 클러스터에 대한 세부 정보를 얻습니다.

## 예제

### 예제 1: 모든 Azure HDInsight 클러스터 나열
```
PS C:\>Get-AzHDInsightCluster
```

이 명령은 모든 Azure HDInsight 클러스터를 나열합니다.

## PARAMETERS

### -ClusterName
클러스터의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -ResourceGroupName
리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster

## 참고 사항

## 관련 링크

[Remove-AzHDInsightCluster](./Remove-AzHDInsightCluster.md)

[Use-AzHDInsightCluster](./Use-AzHDInsightCluster.md)


