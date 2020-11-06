---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/start-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
ms.openlocfilehash: 8c3e0f01472469be856d69c1a87f8eb5185f2012
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536803"
---
# Start-AzureRmHDInsightJob

## SYNOPSIS
지정 된 클러스터에서 정의 된 Azure HDInsight 작업을 시작 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Start-AzureRmHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzureRMHDInsightJob** cmdlet은 지정 된 클러스터에서 정의 된 Azure HDInsight 작업을 시작 합니다.
이는 MapReduce job, 스트리밍 MapReduce 작업, 하이브 작업 또는 문 돼지 job 일 수 있습니다.

## 예제의

### 예제 1: 지정 된 클러스터에서 작업 시작
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

이 명령은-hadoop-001 이라는 클러스터에서 작업을 시작 합니다.

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
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpCredential
클러스터에 대 한 HTTP (클러스터 로그인) 자격 증명을 지정 합니다.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobDefinition
Azure HDInsight 클러스터에서 시작할 작업을 지정 합니다.

```yaml
Type: AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### AzureHDInsightJobDefinition
' JobDefinition ' 매개 변수는 파이프라인에서 ' AzureHDInsightJobDefinition ' 형식의 값을 허용 합니다.

## 출력

### AzureHDInsightJob의. m m.

## 상속자

## 관련 링크

[Get-AzureRmHDInsightJob](./Get-AzureRmHDInsightJob.md)

[새로운 AzureRmHDInsightHiveJobDefinition](./New-AzureRmHDInsightHiveJobDefinition.md)

[중지-AzureRmHDInsightJob](./Stop-AzureRmHDInsightJob.md)

[Wait-AzureRmHDInsightJob](./Wait-AzureRmHDInsightJob.md)


