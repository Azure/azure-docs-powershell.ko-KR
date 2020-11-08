---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 4d5ec07e7a068e1ab96f485ee67db0c1dd43f388
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034350"
---
# Get-AzRecoveryServicesBackupJob

## SYNOPSIS

백업 작업을 가져옵니다.

## 구문과

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은

**AzRecoveryServicesBackupJob** cmdlet은 특정 자격 증명 모음에 대 한 Azure 백업 작업을 가져옵니다.
-VaultId 매개 변수를 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.

## 예제의

### 예제 1: 진행 중인 모든 작업 가져오기

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

첫 번째 명령은 진행 중인 작업의 상태를 배열로 가져온 다음이를 $Joblist 변수에 저장 합니다.
두 번째 명령은 $Joblist 배열의 첫 번째 항목을 표시 합니다.

### 예제 2: 지난 7 일 동안 실패 한 모든 작업 가져오기

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

이 명령은 자격 증명 모음의 마지막 주부터 실패 한 작업을 가져옵니다.
*From* 매개 변수는 UTC에서 지정 된 지난 7 일의 시간을 지정 합니다.
명령에서 *To* 매개 변수에 대 한 값을 지정 하지 않습니다.
따라서 현재 시간에 대 한 기본값을 사용 합니다.

### 예제 3: 진행 중인 작업 가져오기 및 완료 대기

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
$Job = $Jobs[0]
While ( $Job.Status -ne Completed ) {
    Write-Host -Object "Waiting for completion..."
    Start-Sleep -Seconds 10
    $Job = Get-AzRecoveryServicesBackupJob -Job $Job -VaultId $vault.ID
}
Write-Host -Object "Done!"

Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

이 스크립트는 작업이 완료 될 때까지 현재 진행 중인 첫 번째 작업을 폴링합니다.

참고: **Wait-AzRecoveryServicesBackupJob** cmdlet을 사용 하 여 while 루프 대신 Azure Backup 작업이 완료 될 때까지 대기할 수 있습니다.

## 변수

### -BackupManagementType

백업 관리 유형을 지정 합니다.
현재는 Add-azurevm, AzureStorage만 지원 됩니다.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -보낸 사람

이 cmdlet이 가져오는 작업에 대 한 시간 범위의 시작을 **DateTime** 개체로 지정 합니다.
**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.
**DateTime** 개체에 대 한 자세한 내용은를 입력 `Get-Help Get-Date` 합니다.
날짜에 UTC 형식을 사용 합니다.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -작업

가져올 작업을 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId

이 cmdlet이 가져오는 작업의 ID를 지정 합니다.
이 ID는 **Microsoft Azure.** . d m.-To-Commands 기본 개체의 JobId 속성입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -작업

이 cmdlet이 가져오는 작업의 연산을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 백업할
- ConfigureBackup
- DeleteBackupData
- DisableBackup
- 복원한

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobOperation]
Parameter Sets: (All)
Aliases:
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -상태

이 cmdlet이 가져오는 작업의 상태를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- InProgress
- 못함
- 되었습니다
- ...
- 완료
- CompletedWithWarnings

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobStatus]
Parameter Sets: (All)
Aliases:
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -To

이 cmdlet이 가져오는 작업에 대 한 시간 범위의 끝을 **DateTime** 개체로 지정 합니다.
기본값은 현재 시스템 시간입니다.
이 매개 변수를 지정 하는 경우 **-From** 매개 변수도 지정 해야 합니다.
날짜에 UTC 형식을 사용 합니다.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

## 출력

### Microsoft Azure.. i m.. i a m.

## 상속자

## 관련 링크

[Get-AzRecoveryServicesBackupJobDetail](./Get-AzRecoveryServicesBackupJobDetail.md)

[중지-AzRecoveryServicesBackupJob](./Stop-AzRecoveryServicesBackupJob.md)

[Wait-AzRecoveryServicesBackupJob](./Wait-AzRecoveryServicesBackupJob.md)
