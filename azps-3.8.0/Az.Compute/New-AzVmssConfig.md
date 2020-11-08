---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 3c22f34b1dc4e01cf4e3ea2f2b3f9c6045197734
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033756"
---
# New-AzVmssConfig

## SYNOPSIS
VMSS 구성 개체를 만듭니다.

## 구문과

### DefaultParameterSet (기본값)
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType> [-IdentityId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AssignIdentityParameterSet
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**AzVmssConfig** cmdlet은 구성 가능한 vmss (로컬 가상 관리자 배율 집합) 개체를 만듭니다. VMSS 개체를 구성 하려면 다른 cmdlet이 필요 합니다. 이러한 cmdlet은 다음과 같습니다.
- Set-AzVmssOsProfile
- Set-AzVmssStorageProfile
- Add-AzVmssNetworkInterfaceConfiguration
- Add-AzVmssExtension

## 예제의

### 예제 1: VMSS 구성 개체 만들기
```
PS C:\> $VMSS = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

이 예제에서는 VMSS 구성 개체를 만듭니다. 첫 번째 명령은 **AzVmssConfig** cmdlet을 사용 하 여 vmss 구성 개체를 만들고 결과를 $VMSS 이라는 변수에 저장 합니다. 두 번째 명령은 **새 AzVmss** cmdlet을 사용 하 여 첫 번째 명령에서 만든 vmss 구성 개체를 사용 하는 vmss를 만듭니다.

## 변수

### -Id 할당
시스템에서 가상 머신 크기 조정 집합에 대해 할당 된 id를 지정 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutomaticRepairGracePeriod
VM의 상태 변경으로 인해 자동 복구가 일시 중단 되는 시간입니다. 상태 변경이 완료 된 후에 유예 시간이 시작 됩니다. 이는 예기치 않은 복구 또는 우발적으로 수리 하는 것을 방지 합니다. 기간을 ISO 8601 형식으로 지정 해야 합니다. 기본값은 5 분 (PT5M)입니다.

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

### -AutomaticRepairMaxInstanceRepairsPercent
동시에 복구 되는 가상 컴퓨터의 백분율 (scaleset의 용량)입니다. 기본 값은 20%입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoOSUpgrade
최신 버전의 이미지를 사용할 수 있게 되 면 이동 방식으로 확장 설정 인스턴스에 OS 업그레이드를 자동으로 적용할지 여부를 설정 합니다.

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

### -부팅 진단
가상 컴퓨터 크기 집합 부팅 진단 프로필을 지정 합니다.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.BootDiagnostics
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -DisableAutoRollback
자동 OS 업그레이드 정책에 대 한 자동 롤백 해제

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

### -Enable자동 복구
가상 머신 크기 집합에 대 한 자동 복구를 사용 합니다.

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

### -EnableUltraSSD
하나 이상의 관리 되는 데이터 디스크를 가상 컴퓨터 크기 집합의 UltraSSD_LRS 저장소 계정 형식으로 한 개 이상 사용할 수 있도록 합니다.
저장소 계정 유형이 UltraSSD_LRS 관리 디스크는이 속성을 사용 하도록 설정 된 경우에만 VMSS에 추가할 수 있습니다.

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
확장 집합의 가상 컴퓨터에 대 한 제거 정책을 지정 합니다.

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

### -확장
VMSS에 대 한 확장 정보 개체를 지정 합니다. **Add-AzVmssExtension** cmdlet을 사용 하 여이 개체를 추가할 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HealthProbeId
가상 컴퓨터 크기 집합에서 인스턴스의 상태를 확인 하는 데 사용 되는 부하 분산 장치 프로브 ID를 지정 합니다.
HealthProbeId는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName} ' 형식으로 되어 있습니다.

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
가상 컴퓨터 배율 집합과 연결 된 사용자 id 목록을 지정 합니다.
사용자 id 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} ' 형식으로 팔로 리소스 id를 사용 합니다.

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
가상 컴퓨터 크기 집합에 사용 되는 id 유형을 지정 합니다.
' SystemAssignedUserAssigned ' 형식에는 암시적으로 만든 id와 사용자가 할당 한 id 집합이 모두 포함 됩니다.
' 없음 ' 형식은 가상 컴퓨터 배율 집합에서 id를 제거 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 지정 된 SystemAssigned
- UserAssigned 됨
- SystemAssignedUserAssigned
- 않아야

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LicenseType
라이선스 종류를 지정 합니다 (사용자 고유의 라이선스 시나리오를 가져오는 데 사용).

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

### -위치
VMSS가 만들어지는 Azure 위치를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxPrice
우선 순위가 낮은 VM/VMSS에 대해 지불할 최대 가격을 지정 합니다. 이 가격은 미국 달러입니다. 이 가격은 VM 크기에 대 한 현재의 낮은 우선 순위 가격과 비교 됩니다. 또한 우선 순위가 낮은 VM/VMSS의 생성/업데이트가 수행 될 때 가격이 비교 되 고 maxPrice가 현재 낮은 우선 순위의 가격 보다 더 큰 경우에만 작동 합니다. MaxPrice는 VM/VMSS를 만든 후 현재 낮은 우선 순위의 가격이 maxPrice를 초과 하는 경우 우선 순위가 낮은 VM/VMSS를 제거 하는 데도 사용 됩니다. 가능한 값은 다음과 같습니다. 0 보다 큰 10 진수 값입니다. 예: 0.01538.  -1은 낮은 우선 순위의 VM/VMSS가 가격 이유로 제거 되어서는 안 됨을 나타냅니다. 또한 기본 최대 가격은 사용자가 제공 하지 않는 경우-1입니다.

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

### -NetworkInterfaceConfiguration
VMSS 구성에 대 한 네트워킹 속성을 포함 하는 네트워크 프로필 개체를 지정 합니다.
**Add-AzVmssNetworkInterfaceConfiguration** cmdlet을 사용 하 여이 개체를 추가할 수 있습니다.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsProfile
VMSS 구성에 대 한 운영 체제 속성을 포함 하는 운영 체제 프로필 개체를 지정 합니다.
**Set-AzVmssOsProfile** cmdlet을 사용 하 여이 개체를 설정할 수 있습니다.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -과잉 프로비저닝
Cmdlet이 VMSS를 프로 비전 하 고 있는지 여부를 나타냅니다.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -계획 이름
계획 이름을 지정 합니다.

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

### 계획 제품
계획 제품을 지정 합니다.

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

### -PlanPromotionCode
계획 프로 모션 코드를 지정 합니다.

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

### -계획 Publisher
계획 게시자를 지정 합니다.

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

### -PlatformFaultDomainCount
각 배치 그룹의 오류 도메인 수입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -우선 순위
크기 조정 집합의 가상 machien에 대 한 우선 순위입니다.  ' 일반 ', ' 스폿 ' 및 ' Low ' 값만 지원 됩니다.
' 일반 '은 일반 가상 컴퓨터에 대 한 것입니다.
' 스폿 '은 가상 컴퓨터를 위한 것입니다.
' Low '는 스폿 가상 컴퓨터에도 사용할 수 있지만 ' 스폿 '으로 대체 되었습니다. ' 낮음 ' 대신 ' 스폿 '을 사용 하세요.

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
이 배율 집합에 사용할 근접 배치 그룹의 리소스 id입니다.

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

### -RollingUpgradePolicy
롤링 업그레이드 정책을 지정 합니다.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScaleInPolicy
가상 컴퓨터 배율 집합의 크기 조정을 할 때 따라야 하는 규칙입니다.  사용할 수 있는 값은 ' Default ', ' OldestVM ' 및 ' NewestVM '입니다.  ' Default ' 가상 컴퓨터 배율 집합이에서 크기를 조정 하면 영역에 대해 먼저 배율 집합이 조정 됩니다.  그런 다음, 최대한 다양 한 장애 도메인에 분산 됩니다.  각 장애 도메인 내에서 제거 하도록 선택 된 가상 머신은 확장 기능에서 보호 되지 않는 최신 것입니다.  ' OldestVM ' 가상 컴퓨터 크기 조정 집합을 확장 하는 동안에는 스케일에서 보호 되지 않는 가장 오래 된 가상 컴퓨터가 제거 되도록 선택 됩니다.  영역 가상 컴퓨터 배율 집합의 경우에는 맨 먼저 범위에서 배율 집합이 조정 됩니다.  각 영역 내에서 보호 되지 않는 가장 오래 된 가상 컴퓨터는 제거 하도록 선택 됩니다.  ' NewestVM ' 가상 컴퓨터 배율 집합이 확장 되는 경우에는 스케일에서 보호 되지 않는 최신 가상 컴퓨터가 제거 되도록 선택 됩니다.  영역 가상 컴퓨터 배율 집합의 경우에는 맨 먼저 범위에서 배율 집합이 조정 됩니다.  각 영역 내에서 보호 되지 않는 최신 가상 컴퓨터가 제거 되도록 선택 됩니다.

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

### -Single배치 그룹
단일 배치 그룹을 지정 합니다.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipExtensionsOnOverprovisionedVMs
추가 과잉 프로 비전 된 Vm에서 확장이 실행 되지 않도록 지정 합니다.

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

### -SkuCapacity
VMSS의 인스턴스 수를 지정 합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -서 비 Uname
VMSS의 모든 인스턴스 크기를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -서 고 U계층
VMSS의 계층을 지정 합니다. 이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 표준이
- 기본적

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageProfile
VMSS 구성의 디스크 속성이 포함 된 저장소 프로필 개체를 지정 합니다.
**Set-AzVmssStorageProfile** cmdlet을 사용 하 여이 개체를 설정할 수 있습니다.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 태그
해시 테이블 형태의 키-값 쌍입니다. 예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TerminateScheduledEventNotBeforeTimeoutInMinutes
구성 가능한 기간 (분) 삭제 되는 가상 컴퓨터는 이벤트가 자동으로 승인 되기 전에 종료 예약 된 이벤트를 승인 해야 합니다 (시간 초과).

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TerminateScheduledEvents
예약 된 이벤트 종료 사용

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

### -UpgradePolicyMode
확장 집합의 가상 컴퓨터로 업그레이드 모드를 지정 했습니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 자동 번역
- 수동

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.UpgradeMode]
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
가상 컴퓨터 크기 집합에 대 한 영역 목록을 지정 합니다.

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

### -ZoneBalance
영역 작동이 중단 되는 경우를 대비 하 여 가상 컴퓨터 배포 교차 x 영역을 강제 적용할지 여부

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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### 시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]

### System. 문자열

### System.webserver. 컬렉션 테이블

### 시스템. i i.

### 시스템 Null 허용 ' 1 [[23.0.0.0]. UpgradeMode, Microsoft Azure. 관리., Version = 31bf3856ad364e35, Culture = 중립, PublicKeyToken =]]

### VirtualMachineScaleSetOSProfile를 통해 계산 합니다.

### VirtualMachineScaleSetStorageProfile를 통해 계산 합니다.

### Microsoft VirtualMachineScaleSetNetworkConfiguration []을 (를)

### Microsoft VirtualMachineScaleSetExtension []을 (를)

### System.webserver []

### RollingUpgradePolicy를 통해 계산 합니다.

### System.webserver 매개 변수

### Microsoft. Azure. 관리자. 부팅 진단

### 시스템 Null 허용 ' 1 [[ResourceIdentityType, Microsoft azure. 23.0.0.0, Version =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]

## 출력

### PSVirtualMachineScaleSet의. m a.

## 상속자

## 관련 링크

[Set-AzVmssOsProfile](./Set-AzVmssOsProfile.md)

[Set-AzVmssStorageProfile](./Set-AzVmssStorageProfile.md)

[추가-AzVmssNetworkInterfaceConfiguration](./Add-AzVmssNetworkInterfaceConfiguration.md)

[추가-AzVmssExtension](./Add-AzVmssExtension.md)

[새로운 AzVmss](./New-AzVmss.md)
