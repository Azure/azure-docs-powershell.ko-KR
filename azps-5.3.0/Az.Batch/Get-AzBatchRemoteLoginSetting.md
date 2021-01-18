---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 0e2360e6c4d0ba7d993f1f1aa21feb1b44115e6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494133"
---
# Get-AzBatchRemoteLoginSetting

## SYNOPSIS
계산 노드에 대한 원격 로그온 설정을 얻습니다.

## 구문

### ID(기본값)
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzBatchRemoteLoginSetting** cmdlet은 가상 머신 인프라 기반 풀의 계산 노드에 대한 원격 로그온 설정을 얻습니다.

## 예제

### 예제 1: 풀의 모든 노드에 대한 원격 로그온 설정 확인
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

첫 번째 명령은 **Get-AzBatchAccountKey를** 사용하여 구독에 대한 액세스 키를 포함하는 배치 계정 컨텍스트를 얻습니다.
이 명령은 다음 명령에 사용할 $Context 변수에 컨텍스트를 저장합니다.
두 번째 명령은 **Get-AzBatchComputeNode를** 사용하여 ID ContosoPool이 있는 풀의 각 계산 노드를 얻습니다.
이 명령은 파이프라인 연산자를 사용하여 각 컴퓨터 노드를 현재 cmdlet에 전달합니다.
이 명령은 각 계산 노드에 대한 원격 로그온 설정을 얻습니다.

### 예제 2: 노드에 대한 원격 로그온 설정 얻기
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

첫 번째 명령은 구독에 대한 액세스 키를 포함하는 일괄 처리 계정 컨텍스트를 끈 다음, $Context 변수에 저장합니다.
두 번째 명령은 ID ContosoPool이 있는 풀에 지정된 ID가 있는 계산 노드에 대한 원격 로그온 설정을 얻습니다.

## PARAMETERS

### -BatchContext
이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.
구독에 대한 액세스 키를 포함하는 **BatchAccountContext를** 얻습니다. Get-AzBatchAccountKey cmdlet을 사용하세요.

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
계산 노드를 **PSComputeNode** 개체로 지정합니다. 이 cmdlet은 원격 로그온 설정을 얻습니다.
계산 노드 개체를 얻습니다. Get-AzBatchComputeNode cmdlet을 사용합니다.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNodeId
원격 로그온 설정을 얻을 계산 노드의 ID를 지정합니다.
이 cmdlet이 원격 로그온 설정을 얻을 수 있습니다.

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
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -PoolId
가상 머신을 포함하는 풀의 ID를 지정합니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.Batch. Models.PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## 출력

### Microsoft.Azure.Commands.Batch. Models.PSRemoteLoginSettings

## 참고 사항

## 관련 링크

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchComputeNode](./Get-AzBatchComputeNode.md)

[Get-AzBatchRemoteDesktopProtocolFile](./Get-AzBatchRemoteDesktopProtocolFile.md)

[Azure Batch Cmdlet](/powershell/module/Az.Batch/)
