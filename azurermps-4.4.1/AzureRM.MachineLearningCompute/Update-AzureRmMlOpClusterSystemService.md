---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: fc89ff40c36fc444eec23089288849aa5ffe592c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537120"
---
# Update-AzureRmMlOpClusterSystemService

## SYNOPSIS
Operationalization 클러스터의 시스템 서비스에서 업데이트를 시작 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### Cmdlet 입력 매개 변수에서 시스템 서비스 업데이트를 시작 합니다.
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### PSOperationalizationCluster 인스턴스 정의에서 시스템 서비스 업데이트를 시작 합니다.
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### Azure 리소스 id에서 시스템 서비스 업데이트를 시작 합니다.
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-WhatIf] [-Confirm]
```

## 설명은
시스템 서비스는 operationalization 클러스터와 독립적으로 업데이트할 수 있습니다. 시스템 서비스에서 업데이트를 시작 하려면이 cmdlet을 사용 합니다. 업데이트를 사용할 수 없는 경우 업데이트는 계속 시작 되 고 성공적으로 반환 됩니다. 업데이트가 완료 되 면 시작, 완료 및 성공한 경우 보고서를 보고 합니다.

## 예제의

### 예제 1
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

지정 된 클러스터에서 시스템 서비스 업데이트를 시작 합니다. 

## 변수

### -InputObject
Operationalization cluster 개체입니다.

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Start a system services update from an PSOperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
Operationalization 클러스터의 이름입니다.

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
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
Parameter Sets: Start a system services update from cmdlet input parameters.
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
Parameter Sets: Start a system services update from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## 입력

### MachineLearningCompute. PSOperationalizationCluster/.
### System. 문자열


## 출력

### MachineLearningCompute. PSUpdateSystemServicesResponse/.


## 상속자

## 관련 링크

