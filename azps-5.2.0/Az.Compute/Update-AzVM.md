---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e9ec68d7c3991d7a3eded2566d8e299ddcc36c85
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366983"
---
# Update-AzVM

## SYNOPSIS
Azure 가상 머신의 상태를 업데이트합니다.

## 구문

### ResourceGroupNameParameterSetName(기본값)
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### IdParameterSetName
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Update-AzVM** cmdlet은 Azure 가상 머신의 상태를 가상 머신 개체의 상태로 업데이트합니다.

## 예제

### 예제 1: 가상 머신 업데이트
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

이 명령은 ResourceGroup11에서 $VirtualMachine 가상 머신을 업데이트합니다.
이 명령은 $VirtualMachine 변수에 저장된 가상 머신 개체를 사용하여 $VirtualMachine 업데이트합니다.
가상 머신 개체를 얻습니다. **Get-AzVM** cmdlet을 사용합니다.

## PARAMETERS

### -AsJob
백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.

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

### -HostId
호스트의 ID

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

### -EncryptionAtHost
암호화AtHost 속성은 요청에서 사용자가 가상 머신 또는 가상 머신 확장 집합에 대한 호스트 암호화를 활성화하거나 사용하지 않도록 설정할 수 있습니다. 이렇게 하면 호스트 자체의 리소스/임시 디스크를 포함한 모든 디스크에 대한 암호화가 활성화됩니다. 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
가상 머신의 리소스 ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdentityId
가상 머신과 연결된 사용자 ID 목록을 지정합니다.
사용자 ID 참조는 ARM '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}' 형식의 리소스 ID가 됩니다.

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityType
가상 머신에 사용되는 ID의 유형입니다. 유효한 값은 SystemAssigned, UserAssigned, SystemAssignedUserAssigned 및 None입니다.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPrice
우선 순위가 낮은 VM/VMSS에 대해 지불할 최대 가격을 지정합니다. 이 가격은 미국 달러입니다. 이 가격은 VM 크기에 대한 현재 낮은 우선 순위 가격과 비교됩니다. 또한 우선 순위가 낮은 VM/VMSS를 만들/업데이트할 때 가격을 비교하고 maxPrice가 현재 낮은 우선 순위 가격보다 큰 경우 작업이 성공합니다. 또한 현재 우선 순위가 낮은 가격이 VM/VMSS를 생성한 후 maxPrice를 초과하는 경우 maxPrice는 우선 순위가 낮은 VM/VMSS를 지우는 데도 사용됩니다. 가능한 값은 0보다 큰 모든 10진수 값입니다. 예: 0.01538.  -1은 가격상의 이유로 우선 순위가 낮은 VM/VMSS를 피하지 말아야 한다고 나타냅니다. 또한 사용자가 제공하지 않는 경우 기본 최대 가격은 -1입니다.

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NoWait
작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다. 작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.

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

### -OsDiskWriteAccelerator
OS 디스크에서 WriteAccelerator를 사용할지 또는 사용하지 않도록 설정해야 하는지 여부를 지정합니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProximityPlacementGroupId
이 가상 머신에 사용할 근접 배치 그룹의 리소스 ID입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
가상 머신의 리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
리소스 및 리소스 그룹을 이름-값 쌍 집합으로 태그를 지정할 수 있습니다.
리소스에 태그를 추가하면 리소스 그룹에서 리소스를 함께 그룹화하고 사용자 자신의 보기를 만들 수 있습니다.
각 리소스 또는 리소스 그룹은 최대 15개 태그를 사용할 수 있습니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UltraSSDEnabled
VM에 저장소 계정 유형이 있는 하나 이상의 관리되는 데이터 디스크를 UltraSSD_LRS 수 있는 플래그입니다.
저장소 계정 유형이 UltraSSD_LRS 관리 디스크는 이 속성을 사용하는 UltraSSD_LRS 가상 머신에 추가할 수 있습니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
로컬 가상 머신 개체를 지정합니다.
가상 머신 개체를 얻습니다. Get-AzVM cmdlet을 사용합니다.
이 가상 머신 개체에는 가상 머신에 대한 업데이트된 상태가 포함되어 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```


### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.Boolean

## 출력

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## 참고 사항

## 관련 링크

[Get-AzVM](./Get-AzVM.md)

[New-AzVM](./New-AzVM.md)

[Remove-AzVM](./Remove-AzVM.md)

[Restart-AzVM](./Restart-AzVM.md)

[Start-AzVM](./Start-AzVM.md)

[Stop-AzVM](./Stop-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)


