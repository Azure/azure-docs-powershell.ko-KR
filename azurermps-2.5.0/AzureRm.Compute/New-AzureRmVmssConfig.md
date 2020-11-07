---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssconfig
schema: 2.0.0
ms.openlocfilehash: 4bc4782aaf235f81853a7304861a33ca53a75b45
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882349"
---
# New-AzureRmVmssConfig

## SYNOPSIS
VMSS 구성 개체를 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### DefaultParameterSet (기본값)
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AssignIdentityParameterSet
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmVmssConfig** cmdlet은 구성 가능한 vmss (로컬 가상 관리자 배율 집합) 개체를 만듭니다. VMSS 개체를 구성 하려면 다른 cmdlet이 필요 합니다. 이러한 cmdlet은 다음과 같습니다.

- Set-AzureRmVmssOsProfile
- Set-AzureRmVmssStorageProfile
- Add-AzureRmVmssNetworkInterfaceConfiguration
- Add-AzureRmVmssExtension

## 예제의

### 예제 1: VMSS 구성 개체 만들기
```
PS C:\> $VMSS = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzureRmVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

이 예제에서는 VMSS 구성 개체를 만듭니다. 첫 번째 명령은 **AzureRmVmssConfig** cmdlet을 사용 하 여 vmss 구성 개체를 만들고 결과를 $VMSS 이라는 변수에 저장 합니다. 두 번째 명령은 **새 AzureRmVmss** cmdlet을 사용 하 여 첫 번째 명령에서 만든 vmss 구성 개체를 사용 하는 vmss를 만듭니다.

## 변수

### -Id 할당
시스템에서 가상 머신 크기 조정 집합에 대해 할당 된 id를 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutoOSUpgrade
최신 버전의 이미지를 사용할 수 있게 되 면 이동 방식으로 확장 설정 인스턴스에 OS 업그레이드를 자동으로 적용할지 여부를 설정 합니다.

```yaml
Type: SwitchParameter
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
Type: BootDiagnostics
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -확장
VMSS에 대 한 확장 정보 개체를 지정 합니다. **Add-AzureRmVmssExtension** cmdlet을 사용 하 여이 개체를 추가할 수 있습니다.

```yaml
Type: VirtualMachineScaleSetExtension[]
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
Type: String
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
Type: String[]
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
Type: ResourceIdentityType
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
Type: String
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
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkInterfaceConfiguration
VMSS 구성에 대 한 네트워킹 속성을 포함 하는 네트워크 프로필 개체를 지정 합니다.
**Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet을 사용 하 여이 개체를 추가할 수 있습니다.

```yaml
Type: VirtualMachineScaleSetNetworkConfiguration[]
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
**Set-AzureRmVmssOsProfile** cmdlet을 사용 하 여이 개체를 설정할 수 있습니다.

```yaml
Type: VirtualMachineScaleSetOSProfile
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
Type: Boolean
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
Type: String
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
Type: String
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
Type: String
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
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -우선 순위
확장 집합의 가상 컴퓨터에 대 한 우선 순위를 지정 합니다.

```yaml
Type: String
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
Type: RollingUpgradePolicy
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
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuCapacity
VMSS의 인스턴스 수를 지정 합니다.

```yaml
Type: Int32
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
Type: String
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
Type: String
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
**Set-AzureRmVmssStorageProfile** cmdlet을 사용 하 여이 개체를 설정할 수 있습니다.

```yaml
Type: VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 태그
해시 테이블 형태의 키-값 쌍입니다. 예를 들어:

@ {key0 = "value0", key1 = $null, key2 = "value2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
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
Type: UpgradeMode
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
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### PSVirtualMachineScaleSet의. m a.

## 상속자

## 관련 링크

[Set-AzureRmVmssOsProfile](./Set-AzureRmVmssOsProfile.md)

[Set-AzureRmVmssStorageProfile](./Set-AzureRmVmssStorageProfile.md)

[추가-AzureRmVmssNetworkInterfaceConfiguration](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[추가-AzureRmVmssExtension](./Add-AzureRmVmssExtension.md)

[새로운 AzureRmVmss](./New-AzureRmVmss.md)
