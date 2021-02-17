---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
ms.openlocfilehash: 7274067b2f8daa916a0021f0ea2fd7985e1914ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196932"
---
# Set-AzVmssRollingUpgradePolicy

## SYNOPSIS
VMSS 롤링 업그레이드 정책 속성을 지정합니다.

## 구문

```
Set-AzVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
VMSS 롤링 업그레이드 정책 속성을 지정합니다.

## 예제

### 예제 1
```
PS C:\> Set-AzVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

이 명령은 MaxBatchInstance의 경우 40%, MaxUnhealthyInstance의 경우 35%, MaxUnhealthyUpgradedInstance의 경우 30%, VMSS 로컬 개체에 대한 배치 간 30초 일시 중지 시간을 $vmss.

## PARAMETERS

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

### -MaxBatchInstancePercent
롤링 업그레이드를 통해 동시에 업그레이드될 총 가상 머신 인스턴스의 최대 백분율입니다.
이전 또는 미래의 일괄 처리에서 최대의 이상 인스턴스이기 때문에 안정성을 높이기 위해 일괄 처리의 인스턴스 비율이 감소할 수 있습니다.
값을 지정하지 않으면 20으로 설정됩니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxUnhealthyInstancePercent
업그레이드 결과로 또는 롤링 업그레이드가 중단되기 전에 가상 머신 상태 검사에 의해 이상 상태로 발견되어 동시에 이상이 될 수 있는 확장 집합의 총 가상 머신 인스턴스의 최대 백분율입니다.
이 제약 조건은 일괄 처리를 시작하기 전에 검사됩니다.
값을 지정하지 않으면 20으로 설정됩니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxUnhealthyUpgradedInstancePercent
업그레이드된 가상 머신 인스턴스의 최대 백분율은 상태가 상태가 아쉬운 것으로 나타남
이 검사는 각 일괄 처리가 업그레이드된 후에 진행됩니다.
이 비율을 초과하면 롤링 업데이트가 중단됩니다.
값을 지정하지 않으면 20으로 설정됩니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PauseTimeBetweenBatches
모든 가상 머신에 대한 업데이트를 한 번의 일괄 처리로 완료하고 다음 일괄 처리를 시작하는 사이의 대기 시간입니다.
기간은 ISO 8601 형식으로 지정해야 합니다.
기본값은 0초(PT0S)입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
VMSS 개체를 지정합니다.
New-AzVmssConfig cmdlet을 사용하여 개체를 만들 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.Int32

### System.String

## 출력

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## 참고 사항

## 관련 링크
