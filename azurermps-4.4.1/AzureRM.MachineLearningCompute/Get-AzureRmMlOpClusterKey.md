---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 4dfa855bba7318e85eb855e35227070a55d4ed73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534008"
---
# Get-AzureRmMlOpClusterKey

## SYNOPSIS
Operationalization 클러스터와 연결 된 선택 키를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### Cmdlet 입력 매개 변수에서 operationalization 클러스터의 키를 가져옵니다.
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String>
```

### OperationalizationCluster 인스턴스 정의에서 operationalization 클러스터의 키를 가져옵니다.
```
Get-AzureRmMlOpClusterKey -Cluster <PSOperationalizationCluster>
```

### Azure 리소스 id에서 operationalization 클러스터의 키를 가져옵니다.
```
Get-AzureRmMlOpClusterKey -ResourceId <String>
```

## 설명은
클러스터 속성을 가져올 때 저장소 계정, 컨테이너 레지스트리 및 operationalization 클러스터와 연결 된 기타 서비스의 키가 반환 되지 않습니다. 키를 검색 하기 위한 특정 호출은 중요 한 정보 이기 때문에 이루어져야 합니다.

## 예제의

### 예제 1
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

Operationalization 클러스터와 연결 된 서비스에 대 한 비밀 키를 반환 합니다.

## 변수

### -InputObject
Operationalization cluster 개체입니다.

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Get operationalization cluster's keys from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -이름
Operationalization 클러스터의 이름입니다.

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Operationalization 클러스터에 대 한 Azure 리소스 id입니다.

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## 입력

### MachineLearningCompute. PSOperationalizationCluster/.
System. 문자열


## 출력

### MachineLearningCompute. PSOperationalizationClusterCredentials/.


## 상속자

## 관련 링크

