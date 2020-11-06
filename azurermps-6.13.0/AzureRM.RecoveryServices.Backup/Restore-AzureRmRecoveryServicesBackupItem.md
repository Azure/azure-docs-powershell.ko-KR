---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/restore-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: b454f77bc3ad00ddf604e13672d61a7445c44fed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524328"
---
# Restore-AzureRmRecoveryServicesBackupItem

## SYNOPSIS
백업 항목에 대 한 데이터 및 구성을 복구 시점으로 복원 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### AzureVMParameterSet (기본값)
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureFileParameterSet
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 -ResolveConflict <RestoreFSResolveConfictOption> [-SourceFilePath <String>] [-SourceFileType <SourceFileType>]
 [-TargetStorageAccountName <String>] [-TargetFileShareName <String>] [-TargetFolder <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmRecoveryServicesBackupItem** Cmdlet은 Azure 백업 항목에 대 한 데이터 및 구성을 지정 된 복구 시점으로 복원 합니다.
이 cmdlet은 복구 서비스 자격 증명 모음에서 고객의 저장소 계정으로 복원을 시작 합니다.
복원 작업을 수행 해도 전체 가상 컴퓨터는 복원 되지 않습니다.
디스크 데이터 및 구성 정보를 복원 합니다.
복원 작업이 완료 되 면 가상 컴퓨터를 만들어 시작 해야 합니다.
현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.

## 예제의

### 예제 1: 복구 시점으로 항목 복원
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzureRmRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

첫 번째 명령은 Add-azurevm 유형의 백업 컨테이너를 가져온 다음 $Container 변수에 저장 합니다.
두 번째 명령은 $Container에서 V2VM 이라는 백업 항목을 가져온 다음 $BackupItem 변수에 저장 합니다.
세 번째 명령은 7 일 이전 날짜를 가져온 다음 $StartDate 변수에 저장 합니다.
네 번째 명령은 현재 날짜를 가져온 다음 $EndDate 변수에 저장 합니다.
다섯 번째 명령은 $StartDate 및 $EndDate 필터링 한 특정 백업 항목에 대 한 복구 지점 목록을 가져옵니다.
지정 된 날짜 범위가 지난 7 일입니다.
마지막 명령은 디스크를 DestRG 리소스 그룹의 대상 저장소 계정 DestAccount로 복원 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPoint
가상 컴퓨터를 복원할 복구 지점을 지정 합니다.
**AzureRmRecoveryServicesBackupRecoveryPoint** 개체를 가져오려면 Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet을 사용 합니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResolveConflict
복원 된 항목이 대상에도 있는 경우이를 사용 하 여 덮어쓸지 여부를 나타냅니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConfictOption
Parameter Sets: AzureFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFilePath
파일 공유에서 특정 항목을 복원 하는 데 사용 됩니다. 파일 공유 내에서 복원할 항목의 경로입니다.

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
파일 공유에서 특정 항목을 복원 하는 데 사용 됩니다. 파일 공유 내에서 복원할 항목의 경로입니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
구독에 있는 대상 저장소 계정의 이름을 지정 합니다.
복원 프로세스의 일부로이 cmdlet은이 저장소 계정에 디스크 및 구성 정보를 저장 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountResourceGroupName
구독에서 대상 저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.
복원 프로세스의 일부로이 cmdlet은이 저장소 계정에 디스크 및 구성 정보를 저장 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetFileShareName
파일 공유를 복원할 파일 공유입니다.

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
TargetFileShareName 내에서 파일 공유를 복원 해야 하는 폴더입니다. 변수를 비워 두어 루트 폴더 아래에 복원 합니다.

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
관리 디스크가 복원 되는 리소스 그룹입니다. 관리 디스크가 있는 VM의 백업에 적용 가능

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetStorageAccountName
파일 공유를 복원할 저장소 계정입니다.

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
복구 지점의 디스크가 원래 저장소 계정으로 복원 되는 경우이 스위치를 사용 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId
복구 서비스 자격 증명 모음의 팔 ID입니다.

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
복구 서비스 자격 증명 모음의 위치입니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열
매개 변수: VaultId (ByValue), VaultLocation (ByValue)

### RecoveryPointBase에서. i. i m/.
매개 변수: RecoveryPoint (ByValue)

## 출력

### Microsoft Azure.. i m.. i a m.

## 상속자

## 관련 링크

[백업-AzureRmRecoveryServicesBackupItem](./Backup-AzureRmRecoveryServicesBackupItem.md)

[Get-AzureRmRecoveryServicesBackupItem](./Get-AzureRmRecoveryServicesBackupItem.md)

[Get-AzureRmRecoveryServicesBackupRecoveryPoint](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


