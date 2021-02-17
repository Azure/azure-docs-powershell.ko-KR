---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: cbe1160c691fe128f5f2950d728501b815294c05
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191345"
---
# Restore-AzRecoveryServicesBackupItem

## SYNOPSIS

Backup 항목에 대한 데이터 및 구성을 지정된 복구 지점으로 복원합니다. 필요한 매개 변수는 백업 항목 유형에 따라 다릅니다.
동일한 명령을 사용하여 Azure Virtual Machines, Azure Virtual Machines 내에서 실행되는 데이터베이스 및 Azure 파일 공유도 복원합니다.

## 구문

### AzureVMParameterSet(기본값)
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AzureVMManagedDiskParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureVMRestoreManagedAsUnmanaged
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureVMUnManagedDiskParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureFileShareParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureWorkloadParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase> [-RestoreToSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명

**Restore-AzRecoveryServicesBackupItem** cmdlet은 Azure Backup 항목에 대한 데이터 및 구성을 지정된 복구 지점으로 복원합니다.

**Azure VM 백업의 경우**

이 명령을 사용하여 Azure 가상 머신을 백업하고 디스크(관리 및 관리되지 않는 디스크 모두)를 복원할 수 있습니다. 복원 작업은 전체 가상 머신을 복원하지 않습니다.
관리 디스크 VM인 경우 복원된 디스크가 보관되는 대상 리소스 그룹을 지정해야 합니다. 대상 리소스 그룹을 지정하면 스냅숏이 백업 정책에 지정된 리소스 그룹에 있는 경우 복원 작업은 즉시 수행됩니다. 디스크는 로컬 스냅숏에서 만들어지며 대상 리소스 그룹에 보관됩니다. 관리되지 않는 디스크로 복원하는 옵션도 있지만 Azure Recovery Services 자격 증명 모음에 있는 데이터를 활용하기 때문에 속도가 매우 느려질 수 있습니다. 복원된 디스크에서 VM을 만드는 데 사용할 수 있는 VM 및 배포 템플릿의 구성이 지정된 저장소 계정에 다운로드됩니다.
관리되지 않는 디스크 VM인 경우 스냅숏은 디스크의 원래 저장소 계정 및/또는 복구 서비스 자격 증명 모음에 있습니다. 사용자가 원본 저장소 계정을 사용하여 복원할 수 있는 옵션을 제공하는 경우 즉시 복원을 제공하면 됩니다. 그렇지 않으면 Azure Recovery Services 자격 증명 모음에서 데이터를 페치하고 VM 및 배포 템플릿의 구성과 함께 디스크가 지정된 저장소 계정에 만들어집니다.

> [!IMPORTANT]
> 기본적으로 Azure VM 백업은 모든 디스크를 백업합니다. Enable-Backup 중에 exclusionList 또는 InclusionList 매개 변수를 사용하여 관련 디스크를 선택적으로 백업할 수 있습니다. 디스크를 선택적으로 복원하는 옵션은 디스크를 선택적으로 백업한 경우만 사용할 수 있습니다.

자세한 내용은 가능한 다른 매개 변수 집합 및 매개 변수 텍스트를 참조하세요.

> [!NOTE]
> -VaultId 매개 변수를 사용하는 경우 -VaultLocation 매개 변수도 사용해야 합니다.

**Azure 파일 공유 백업의 경우**

전체 파일 공유 또는 공유의 특정/여러 파일/폴더를 복원할 수 있습니다. 원래 위치 또는 대체 위치로 복원할 수 있습니다.

**Azure 워크로드의 경우**

Azure VM 내에서 SQL DB를 복원할 수 있습니다.


## 예제

### 예제 1: 주어진 복구 지점에서 백업된 Managed Disks Azure VM의 디스크 복원

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

첫 번째 명령은 Recovery Services 자격 증명 모음을 얻게 하여 변수에 $vault 저장합니다.
두 번째 명령은 이름 "V2VM"의 AzureVM 형식의 Backup 항목을 $BackupItem 변수에 저장합니다.
세 번째 명령은 날짜를 7일 전의 날짜로 하여 $StartDate 변수에 저장합니다.
네 번째 명령은 현재 날짜를 인용한 다음, $EndDate 저장합니다.
다섯 번째 명령은 특정 백업 항목에 대한 복구 지점 목록을 $StartDate $EndDate.
마지막 명령은 모든 디스크를 대상 리소스 그룹 Target_RG 복원한 다음, DestRG 리소스 그룹의 저장소 계정 DestAccount에서 VM 구성 정보 및 배포 템플릿을 제공합니다.

### 예제 2: 지정된 복구 지점에서 백업된 Managed Disks Azure VM의 지정된 디스크 복원

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

첫 번째 명령은 Recovery Services 자격 증명 모음을 얻게 하여 변수에 $vault 저장합니다.
두 번째 명령은 이름 "V2VM"의 AzureVM 형식의 Backup 항목을 $BackupItem 변수에 저장합니다.
세 번째 명령은 날짜를 7일 전의 날짜로 하여 $StartDate 변수에 저장합니다.
네 번째 명령은 현재 날짜를 인용한 다음, $EndDate 저장합니다.
다섯 번째 명령은 특정 백업 항목에 대한 복구 지점 목록을 $StartDate $EndDate.
여섯 번째 명령은 restoreDiskLUN 변수에 복원할 디스크 목록을 저장합니다.
마지막 명령은 지정된 LUNS의 지정된 디스크를 대상 리소스 그룹 Target_RG 복원한 다음, DestRG 리소스 그룹의 저장소 계정 DestAccount에 VM 구성 정보 및 배포 템플릿을 제공합니다.

### 예제 3: 관리되는 VM의 디스크를 관리되지 않는 디스크로 복원

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

첫 번째 명령은 RecoveryServices 자격 증명 모음을 사용하여 $vault 저장합니다.
두 번째 명령은 Backup 항목을 인용한 다음, 백업 $BackupItem 저장합니다.
세 번째 명령은 날짜를 7일 전의 날짜로 하여 $StartDate 변수에 저장합니다.
네 번째 명령은 현재 날짜를 인용한 다음, $EndDate 저장합니다.
다섯 번째 명령은 특정 백업 항목에 대한 복구 지점 목록을 $StartDate $EndDate.
여섯 번째 명령은 디스크를 관리되지 않는 디스크로 복원합니다.

### 예제 4: 원래 저장소 계정을 사용하여 관리되지 않는 VM을 관리되지 않는 디스크로 복원

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -Name "UnManagedVM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

첫 번째 명령은 RecoveryServices 자격 증명 모음을 사용하여 $vault 저장합니다.
두 번째 명령은 Backup 항목을 인용한 다음, 백업 $BackupItem 저장합니다.
세 번째 명령은 날짜를 7일 전의 날짜로 하여 $StartDate 변수에 저장합니다.
네 번째 명령은 현재 날짜를 인용한 다음, $EndDate 저장합니다.
다섯 번째 명령은 특정 백업 항목에 대한 복구 지점 목록을 $StartDate $EndDate.
여섯 번째 명령은 디스크를 원래 저장소 계정에 관리되지 않는 디스크로 복원합니다.

### 예제 5: AzureFileShare 항목의 여러 파일 복원

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem   Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

첫 번째 명령은 Recovery Services 자격 증명 모음을 얻게 하여 변수에 $vault 저장합니다.
두 번째 명령은 fileshareitem이라는 Backup 항목을 다운로드한 다음, $BackupItem 변수에 저장합니다.
세 번째 명령은 특정 백업 항목에 대한 복구 지점 목록을 얻습니다.
네 번째 명령은 복원할 파일을 지정하고 변수에 $files 지정합니다.
마지막 명령은 지정된 파일을 원래 위치로 복원합니다.

### 예제 6: Azure VM 내의 SQL DB를 고유한 전체 복구 지점에 대한 다른 대상 VM으로 복원

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $FullRP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithFullConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -RecoveryPoint $FullRP -TargetItem $TargetInstance -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName       Operation        Status            StartTime                 EndTime          JobID
    ------------       ---------        ------            ---------                 -------          -----
    MSSQLSERVER/m...   Restore          InProgress        3/17/2019 10:02:45 AM                      3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

### 예제 7: Azure VM 내의 SQL DB를 로그 복구 지점에 대한 다른 대상 VM으로 복원

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $PointInTime = Get-Date -Date "2019-03-20 01:00:00Z"
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithLogConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -PointInTime $PointInTime -Item $BackupItem -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName     Operation      Status           StartTime                 EndTime           JobID
    ------------     ---------      ------           ---------                 -------           -----
    MSSQLSERVER/m... Restore        InProgress       3/17/2019 10:02:45 AM                       3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

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

### -MultipleSourceFilePath
파일 공유에서 여러 파일을 복원하는 데 사용됩니다. 파일 공유 내에서 복원할 항목의 경로입니다.

```yaml
Type: System.String[]
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPoint

백업 항목을 복원할 복구 지점을 지정합니다.
**AzureRmRecoveryServicesBackupRecoveryPoint** 개체를 얻습니다. **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet을 사용합니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResolveConflict

복원된 항목도 대상에 있는 경우 이 항목을 사용하여 덮어 사용할지 여부를 나타냅니다.
이 매개 변수에 허용되는 값은

- 덮어덮어
- 건너뛰기

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConflictOption
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: Overwrite, Skip

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreAsUnmanagedDisks
이 스위치를 사용하여 관리되지 않는 디스크로 복원

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMRestoreAsUnmanaged
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreDiskList
백업된 VM을 복구할 디스크 지정

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreOnlyOSDisk
이 스위치를 사용하여 백업된 VM의 OS 디스크만 복원

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFilePath

파일 공유에서 특정 항목 복원에 사용됩니다. 파일 공유 내에서 복원할 항목의 경로입니다.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFileType

파일 공유에서 특정 항목 복원에 사용됩니다. 파일 공유 내에서 복원할 항목의 유형입니다.
이 매개 변수에 허용되는 값은

- 파일
- 디렉터리

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType]
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: File, Directory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName

구독에서 대상 Storage 계정의 이름을 지정합니다.
복원 프로세스의 일부로 이 cmdlet은 디스크 및 구성 정보를 이 Storage 계정에 저장합니다.

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountResourceGroupName

구독에 대상 Storage 계정을 포함하는 리소스 그룹의 이름을 지정합니다.
복원 프로세스의 일부로 이 cmdlet은 디스크 및 구성 정보를 이 Storage 계정에 저장합니다.

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetFileShareName

파일 공유를 복원해야 하는 파일 공유입니다.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetFolder

TargetFileShareName 내에서 파일 공유를 복원해야 하는 폴더입니다. 백업된 콘텐츠를 루트 폴더로 복원하는 경우 대상 폴더 값을 빈 문자열로 제공합니다.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetResourceGroupName

관리 디스크가 복원되는 리소스 그룹입니다. 관리 디스크가 있는 VM의 백업에 적용 가능

```yaml
Type: System.String
Parameter Sets: AzureVMTargetRGParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetStorageAccountName

파일 공유를 복원해야 하는 저장소 계정입니다.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseOriginalStorageAccount

복구 지점의 디스크를 원래 저장소 계정으로 복원할 경우 이 스위치를 사용 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskEncryptionSetId 

복원된 디스크를 암호화하는 DES ID입니다.

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMManagedDiskParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreToSecondaryRegion

이 스위치를 사용하여 보조 지역으로 지역 간 복원을 트리거합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIaasVM
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId

ARM 자격 증명 모음의 ID입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VaultLocation

Recovery Services 자격 증명 모음의 위치입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WLRecoveryConfig

복구 구성

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase
Parameter Sets: AzureWorkloadParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### System.String

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase

## 출력

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase

## 참고 사항

## 관련 링크

[Backup-AzRecoveryServicesBackupItem](./Backup-AzRecoveryServicesBackupItem.md)

[Get-AzRecoveryServicesBackupItem](./Get-AzRecoveryServicesBackupItem.md)

[Get-AzRecoveryServicesBackupRecoveryPoint](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
