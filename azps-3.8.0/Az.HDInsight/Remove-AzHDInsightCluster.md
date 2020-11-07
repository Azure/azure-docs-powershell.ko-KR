---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: c4a3f33094e5337306e44e2b310cd7cce32e8887
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879758"
---
# Remove-AzHDInsightCluster

## SYNOPSIS
현재 구독에서 지정 된 HDInsight 클러스터를 제거 합니다.

## 구문과

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzHDInsightCluster** cmdlet은 지정 된 HDInsight 서비스 클러스터를 구독에서 제거 합니다.
또한이 작업은 클러스터의 Hadoop 분산 파일 시스템 (HDFS)에 저장 된 모든 데이터를 삭제 합니다.
연결 된 Azure 저장소 계정에 저장 된 데이터는 삭제 되지 않습니다.
외부 metastores에 저장 된 데이터는 삭제 되지 않습니다.

## 예제의

### 예제 1: Azure HDInsight 클러스터 삭제
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

이 명령은-hadoop-001 이라는 클러스터를 제거 합니다.

## 변수

### -ClusterName
클러스터의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: IAzureContextContainer
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
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
PassThru가 있는 경우 결과를 출력 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### 않아야
## 출력

### 시스템 부울
## 상속자

## 관련 링크

[Get-AzHDInsightCluster](./Get-AzHDInsightCluster.md)

[-AzHDInsightCluster 사용](./Use-AzHDInsightCluster.md)


