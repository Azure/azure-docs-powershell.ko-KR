---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: 8b15a93ee576af683cb2ebfffa621937a2ebba78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868290"
---
# Get-AzHDInsightCluster

## SYNOPSIS
현재 구독 또는 지정 된 리소스 그룹과 연결 된 모든 Azure HDInsight 클러스터를 가져오고 나열 하거나 특정 클러스터를 검색 합니다.

## 구문과

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzHDInsightCluster** cmdlet은 현재 구독에 대 한 Azure HDInsight 서비스 클러스터를 나열 합니다.
특정 클러스터에 대 한 세부 정보를 가져오려면 *ClusterName* 매개 변수를 사용 합니다.

## 예제의

### 예제 1: 모든 Azure HDInsight 클러스터 나열
```
PS C:\>Get-AzHDInsightCluster
```

이 명령은 모든 Azure HDInsight 클러스터를 나열 합니다.

## 변수

### -ClusterName
클러스터의 이름을 지정 합니다.

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
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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
리소스 그룹의 이름을 지정 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### AzureHDInsightCluster의. m m.

## 상속자

## 관련 링크

[제거-AzHDInsightCluster](./Remove-AzHDInsightCluster.md)

[-AzHDInsightCluster 사용](./Use-AzHDInsightCluster.md)


