---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
ms.openlocfilehash: aaf020d61941057dd0dabac849adb37197e02882
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987009"
---
# New-AzBatchComputeNodeUser

## SYNOPSIS
Batch 계산 노드에 사용자 계정을 만듭니다.

## 구문

### ID
```
New-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentObject
```
New-AzBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**New-AzBatchComputeNodeUser** cmdlet은 Azure Batch 계산 노드에 사용자 계정을 만듭니다.

## 예제

### 예제 1: 관리 자격 증명이 있는 사용자 계정 만들기
```
PS C:\>New-AzBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

이 명령은 ID ComputeNode01이 있는 계산 노드에 사용자 계정을 만듭니다.
노드는 Id MyPool01이 있는 풀에 있습니다.
사용자 이름은 TestUser, 암호는 암호, 계정은 7일 후에 만료되고 계정에 관리 자격 증명이 있습니다.

### 예제 2: 파이프라인을 사용하여 계산 노드에서 사용자 계정 만들기
```
PS C:\>Get-AzBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

이 명령은 **Get-AzBatchComputeNode** cmdlet을 사용하여 ComputeNode01이라는 계산 노드를 얻습니다.
해당 노드는 ID MyPool01이 있는 풀에 있습니다.
명령은 파이프라인 연산자를 사용하여 해당 계산 노드를 현재 cmdlet에 전달합니다.
명령은 사용자 이름 TestUser 및 암호 암호가 있는 사용자 계정을 만듭니다.

## 매개 변수

### -BatchContext
Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.
Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다. 대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다. 공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다. 사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNode
이 cmdlet에서 사용자 계정을 만드는 **PSComputeNode** 개체로 계산 노드를 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNodeId
이 cmdlet에서 사용자 계정을 만드는 계산 노드의 ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -ExpiryTime
새 사용자 계정에 대한 만료 시간을 지정합니다.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsAdmin
cmdlet이 관리 자격 증명이 있는 사용자 계정을 만듭니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
새 로컬 Windows 계정의 이름을 지정합니다.

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

### -Password
사용자 계정 암호를 지정합니다.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
사용자 계정을 만들 계산 노드가 포함된 풀의 ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.Commands.Bat. Models.PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## 출력

### System.Void

## 참고 사항

## 관련 링크

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchComputeNode](./Get-AzBatchComputeNode.md)

[Remove-AzBatchComputeNodeUser](./Remove-AzBatchComputeNodeUser.md)

[Azure Batch Cmdlet](/powershell/module/Az.Batch/)
