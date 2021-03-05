---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 71aa555528ff1cdb5748c1a4ac62481ddd17c17c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991494"
---
# New-AzVMConfig

## SYNOPSIS
구성 가능한 가상 머신 개체를 만듭니다.

## 구문

### DefaultParameterSet(기본값)
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**New-AzVMConfig** cmdlet은 Azure에 대해 구성 가능한 로컬 가상 머신 개체를 만듭니다.
다른 cmdlet을 사용하여 Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface 및 Set-AzVMOSDisk와 같은 가상 머신 개체를 구성할 수 있습니다.

## 예제

### 예제 1: 가상 머신 개체 만들기
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

첫 번째 명령은 ResourceGroup11이라는 리소스 그룹에서 AvailabilitySet03이라는 가용성 집합을 얻은 다음, 해당 개체를 $AvailabilitySet 저장합니다.
두 번째 명령은 가상 머신 개체를 만든 다음, 가상 머신 개체를 $VirtualMachine 변수에 저장합니다.
명령은 가상 머신에 이름과 크기를 할당합니다.
가상 머신은 가상 머신에 저장된 가용성 집합에 $AvailabilitySet.

## 매개 변수

### -AvailabilitySetId
가용성 집합의 ID를 지정합니다.
가용성 집합 개체를 얻은 경우 Get-AzAvailabilitySet cmdlet을 사용합니다.
가용성 집합 개체에는 ID 속성이 포함되어 있습니다. <br>
동일한 가용성 집합에 지정된 가상 머신은 가용성을 최대화하기 위해 서로 다른 노드에 할당됩니다. <br>
가용성 집합에 대한 자세한 내용은 가상 [머신의 가용성 관리를 참조하세요.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json) <br>
Azure 계획된 유지 관리에 대한 자세한 내용은 Azure의 가상 머신에 [대한 계획된 유지 관리 를 참조하세요.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json) <br>
현재 VM은 생성 시 가용성 집합에만 추가할 수 있습니다. VM이 추가되는 가용성 집합은 가용성 집합 리소스와 동일한 리소스 그룹 아래에 있습니다. 기존 VM을 가용성 집합에 추가할 수 없습니다. <br>
이 속성은 null이 아닌 속성.virtualMachineScaleSet 참조와 함께 존재할 수 없습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -EnableUltraSSD
VM에 저장소 계정 유형이 있는 하나 이상의 관리되는 데이터 UltraSSD_LRS 기능을 사용할 수 있습니다.
저장소 계정 유형이 있는 관리 UltraSSD_LRS 이 속성을 사용하도록 설정한 경우 가상 머신에 추가할 수 있습니다.


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EvictionPolicy
Azure Spot 가상 머신에 대한 eviction 정책입니다.  지원되는 값은 'Deallocate' 및 'Delete'입니다.

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

### -IdentityId
가상 머신 확장 집합과 연결된 사용자 ID 목록을 지정합니다.
사용자 ARM ID 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}' 형식의 리소스 ID로 설정됩니다.

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdentityType
구성된 경우 가상 머신의 ID입니다.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseType
가상 머신의 이미지 또는 디스크가 On-프레미스에 라이선스가 부여된 경우를 나타내는 라이선스 유형을 지정합니다.
Windows Server의 가능한 값은:
- Windows_Client
- Windows_Server Linux Server 운영 체제에 대한 가능한 값은 다음입니다. 
- RHEL_BYOS(RHEL용) 
- SLES_BYOS(SUSE용) 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPrice
우선 순위가 낮은 VM/VMSS에 대해 지불할 최대 가격을 지정합니다. 이 가격은 미국 달러입니다. 이 가격은 VM 크기에 대한 현재 낮은 우선 순위 가격과 비교됩니다. 또한 가격은 우선 순위가 낮은 VM/VMSS를 만들/업데이트할 때 비교하며, maxPrice가 현재 낮은 우선 순위 가격보다 큰 경우 작업이 성공합니다. 현재 낮은 우선 순위 가격이 VM/VMSS를 생성한 후 maxPrice를 초과하는 경우, maxPrice는 우선 순위가 낮은 VM/VMSS를 지우는 데도 사용됩니다. 가능한 값은 0보다 큰 소수점 값입니다. 예: 0.01538입니다.  -1은 가격상의 이유로 우선 순위가 낮은 VM/VMSS를 아 내지 말아야 한다고 나타냅니다. 또한 기본 최대 가격은 사용자가 제공하지 않는 경우 -1입니다.

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

### -EncryptionAtHost
EncryptionAtHost 속성은 요청에서 사용자가 가상 머신 또는 가상 머신 확장 집합에 대한 호스트 암호화를 사용하도록 설정하거나 사용하지 않도록 설정할 수 있습니다. 이렇게 하면 호스트 자체에서 Resource/Temp 디스크를 포함하여 모든 디스크에 대한 암호화가 활성화됩니다. 기본값: 이 속성이 리소스에 대해 true로 설정되지 않는 한 호스트의 암호화를 사용하지 않도록 설정됩니다.

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

### -Priority
가상 머신의 우선 순위입니다.  지원되는 값만 '일반', 'Spot' 및 'Low'입니다.
'일반'은 일반 가상 머신용입니다.
'Spot'은 가상 머신을 위한 것입니다.
'Low'은 스팟 가상 머신용이지만 'Spot'으로 바 대체됩니다. 'Low' 대신 'Spot'을 사용하세요.

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

### -ProximityPlacementGroupId
이 가상 머신에서 사용할 근접 배치 그룹의 리소스 ID입니다.

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

### -Tags
리소스에 연결된 태그입니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
가상 머신의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSize
가상 머신의 크기를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmssId
가상 머신 확장 집합의 ID

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

### -Zone
가상 머신에 대한 가용성 영역 목록을 지정합니다. 허용되는 값은 지역의 기능에 따라 달라 습니다. 허용되는 값은 일반적으로 1,2,3입니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

### System.String[]

### System.Collections.Hashtable

### System.Management.Automation.SwitchParameter

## 출력

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## 참고 사항

## 관련 링크

[Update-AzVM](./Update-AzVM.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)

[Set-AzVMSourceImage](./Set-AzVMSourceImage.md)

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)


