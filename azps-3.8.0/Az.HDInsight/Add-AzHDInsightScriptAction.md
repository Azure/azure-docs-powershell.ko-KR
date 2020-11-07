---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
ms.openlocfilehash: d103a2bc3d23ff37857592ed9496e625302ed144
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879841"
---
# Add-AzHDInsightScriptAction

## SYNOPSIS
클러스터 구성 개체에 스크립트 작업을 추가 합니다.

## 구문과

```
Add-AzHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzHDInsightScriptAction** cmdlet은 New-AzHDInsightClusterConfig cmdlet에서 만든 HDInsight 구성 개체에 스크립트 작업을 추가 합니다.
스크립트 동작은 추가 소프트웨어를 설치 하거나 Windows PowerShell 또는 Bash 스크립트 (Windows 또는 Linux 클러스터의 경우)를 사용 하 여 Hadoop 클러스터에서 실행 되는 응용 프로그램의 구성을 변경 하는 데 사용 되는 기능을 제공 합니다.
HDInsight 클러스터를 배포할 때 클러스터 노드에서 스크립트 작업을 실행 하 고 클러스터 전체 HDInsight 구성의 노드 이후 실행 합니다.
스크립트 동작은 시스템 관리자 계정 권한으로 실행 되며 클러스터 노드에 대 한 전체 액세스 권한을 제공 합니다.
각 클러스터에 대해 지정 된 순서로 실행할 스크립트 작업 목록을 제공할 수 있습니다.

## 예제의

### 예제 1: 클러스터 구성 개체에 스크립트 동작 추가
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Script action info
PS C:\> $scriptActionName = "<script action name>"
PS C:\> $scriptActionURI = "<script action URI>"
PS C:\> $scriptActionParameters = "<script action parameters>" 

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Worker `
            | Add-AzHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Head `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

이 명령은 클러스터 생성 종료 시 실행 될 hadoop-001 클러스터의 Head 및 Worker 노드에 대 한 스크립트 동작을 추가 합니다.

## 변수

### -구성
이 cmdlet이 수정 하는 HDInsight 클러스터 구성 개체를 지정 합니다.
이 개체는 **AzHDInsightClusterConfig** cmdlet에서 생성 됩니다.

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### -이름
스크립트 작업의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodeType
스크립트 작업을 실행할 노드 형식을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 인원 노드
- . 노드
- ZookeeperNode

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -매개 변수
스크립트 작업에 대 한 매개 변수를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Uri
스크립트 작업 (PowerShell 또는 Bash 스크립트)에 대 한 공용 URI를 지정 합니다.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### AzureHDInsightConfig의. m m.

## 출력

### AzureHDInsightConfig의. m m.

## 상속자

## 관련 링크

[새로운 AzHDInsightClusterConfig](./New-AzHDInsightClusterConfig.md)


