---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 1b5f447e95e137ba9199ba596029f2088a977c91
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490780"
---
# Set-AzRecoveryServicesAsrReplicationProtectedItem

## SYNOPSIS
지정된 복제 보호 항목에 대한 대상 네트워크 및 가상 머신 크기와 같은 복구 속성을 설정합니다.

## 구문

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryProximityPlacementGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
**Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet은 복제 보호된 항목에 대한 복구 속성을 설정합니다.

## 예제

### 예제 1
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

지정된 매개 변수를 사용하여 복제 보호된 항목 설정을 업데이트하는 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.

### 예제 2
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

지정된 매개 변수를 사용하여 복제 보호 항목 네트워크 인터페이스 카드(NIC 감소) 설정을 업데이트하는 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.

### 예제 3
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

지정된 매개 변수를 사용하여 복제 보호된 항목 기본 NIC(복구된 vm )설정 업데이트 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.

### 예제 4
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

지정된 매개 변수를 사용하여 복제 보호된 항목 NIC(복구된 vm 설정에 사용)를 업데이트하는 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.

### 예제 5
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

선택한 noc tp를 사용하여 복구 VM(Azure에서 Azure로 재해 복구)에서 가속화된 네트워킹을 사용하도록 선택한 복제 보호 항목을 업데이트하는 작업을 시작합니다.
가속 네트워킹을 사용하지 않도록 설정하려면 -EnableAcceleratedNetworkingOnRecovery를 전달하지 않습니다.

### 예제 6
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

지정된 암호화된 복제 보호 항목에 대한 업데이트 작업을 시작하여 장애 조치(failover) VM에 제공된 암호화 세부 정보를 사용합니다.

### 예제 7
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

지정된 복제 보호 항목에 대한 업데이트 작업을 시작하여 장애 조치(failover) VM에 제공된 근접 배치 그룹을 사용합니다.


## PARAMETERS

### -ASRVMNicConfiguration
테스트 장애 조치(failover) 및 장애 조치(failover) NIC 구성 세부 정보를 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureToAzureUpdateReplicationConfiguration
관리 디스크 VM에 대해 udpated할 디스크 구성을 지정합니다(Azure에서 Azure DR scenrio로).

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
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

### -DiskEncryptionSecretUrl
장애 조치(failover) 후 복구 VM으로 사용할 버전(Azure 디스크 암호화)을 사용하여 디스크 암호화 비밀 URL을 지정합니다.

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

### -DiskEncryptionVaultId
장애 조치(failover) 후 복구 VM으로 사용할 디스크 암호화 비밀 키 자격 증명 모음 ID(Azure Disk Encryption)를 지정합니다.

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

### -DiskIdToDiskEncryptionSetMap
디스크 리소스 ID에서 디스크 암호화 집합으로의 사전 ARM ID입니다.

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAcceleratedNetworkingOnRecovery
장애 조치(failover)가 가속화된 네트워킹을 사용하여 복구 VM에 지정된 NIC를 지정합니다.

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

### -InputObject
cmdlet에 대한 입력 개체: 업데이트할 복제 보호 항목에 해당하는 ASR 복제 보호된 항목 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyEncryptionKeyUrl
장애 조치(failover) 후 복구 VM으로 사용할 디스크 암호화 키 URL 버전(Azure 디스크 암호화)을 지정합니다.

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

### -KeyEncryptionVaultId
장애 조치(failover) 후 복구 VM으로 사용할 디스크 암호화 keyVault ID(Azure Disk Encryption)를 지정합니다.


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

### -LicenseType
Windows Server 가상 머신에 사용할 라이선스 유형 선택을 정합니다. 마이그레이션에 Azure HUB(하이브리드 사용 혜택)를 사용할 자격이 있으며 이 보호된 항목을 장애 조치하는 동안 허브 설정을 사용할 수 있도록 지정하려는 경우 라이선스 유형을 WindowsServer로 설정하세요.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
장애 조치(failover) 시 만들 복구 가상 머신의 이름을 지정합니다.

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

### -NicSelectionType
사용자가 설정하거나 기본적으로 설정한 NIC(네트워크 인터페이스 카드) 속성을 지정합니다.
NotSelected를 지정하여 기본값으로 돌아갈 수 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryNic
장애 조치(failover) 후 재구성 VM에 대한 기본 NIC로 사용할 NIC를 지정합니다.

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

### -RecoveryAvailabilitySet
장애 조치(failover) 후 복제 보호 항목에 대한 가용성 집합입니다.

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

### -RecoveryBootDiagStorageAccountId
복구 Azure VM에 대한 부팅 진단을 위한 저장소 계정을 지정합니다.

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

### -RecoveryCloudServiceId
이 가상 머신을 장애 조치(failover)할 복구 클라우드 서비스의 리소스 ID입니다.

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

### -RecoveryLBBackendAddressPoolId
복구 NIC와 연결될 대상 백안 주소 풀을 지정합니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryNetworkId
보호된 항목을 실패해야 하는 Azure 가상 네트워크의 ID를 지정합니다.

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

### -RecoveryNetworkSecurityGroupId
복구 NIC와 연결될 네트워크 보안 그룹의 ID를 지정합니다.

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

### -RecoveryNicStaticIPAddress
복구 시 기본 NIC에 할당해야 하는 고정 IP 주소를 지정합니다.

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

### -RecoveryNicSubnetName
장애 조치 시 보호된 항목의 이 NIC를 연결해야 하는 복구 Azure 가상 네트워크의 서브넷 이름을 지정합니다.

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

### -RecoveryProximityPlacementGroupId
가상 머신을 장애 조치할 복구 근접 배치 그룹의 리소스 ID를 지정합니다.

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

### -RecoveryPublicIPAddressId
복구 NIC와 연결될 공용 IP 주소 리소스의 ID를 지정합니다.

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

### -RecoveryResourceGroupId
장애 조치 시 보호된 항목을 복구할 복구 지역의 Azure 리소스 그룹의 ID입니다.

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

### -Size
복구 가상 머신 크기를 지정합니다.
값은 Azure 가상 머신에서 지원하는 크기 집합에서 제공해야 합니다.

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

### -TfoAzureVMName
테스트 장애 조치(failover) VM의 이름을 지정합니다.

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

### -UpdateNic
이 cmdlet이 복구 네트워크 속성을 udpated해야 하는 가상 머신의 NIC를 지정합니다.

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

### -UseManagedDisk
장애 조치(failover)에 생성된 Azure 가상 머신이 관리 디스크를 사용할지 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
cmdlet이 실행되는 경우의 결과 표시 cmdlet이 실행되지 않습니다.

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

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem

## 출력

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob

## 참고 사항

## 관련 링크

[Get-AzRecoveryServicesAsrReplicationProtectedItem](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[New-AzRecoveryServicesAsrReplicationProtectedItem](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[Remove-AzRecoveryServicesAsrReplicationProtectedItem](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
