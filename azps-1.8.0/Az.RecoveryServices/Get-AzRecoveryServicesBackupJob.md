---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 5dab5eaca48152dc573caf75f5d80737802bfcdf
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399824"
---
# Get-AzRecoveryServicesBackupJob

## SYNOPSIS
Backup 작업을 얻습니다.

## 구문

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzRecoveryServicesBackupJob** cmdlet은 특정 자격 증명 모음에 대한 Azure Backup 작업을 얻습니다.
현재 cmdlet을 사용하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용하여 자격 증명 모음 컨텍스트를 설정할 수 있습니다.

## 예제

### 예제 1: 진행 중 작업 모두를 얻습니다.
```
PS C:\>$Joblist = Get-AzRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

첫 번째 명령은 진행 중 작업의 상태를 배열로 하여 $Joblist 변수에 저장합니다.
두 번째 명령은 배열의 첫 번째 $Joblist 표시됩니다.

### 예제 2: 지난 7일 동안 실패한 모든 작업 얻기
```
PS C:\>Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

이 명령은 자격 증명 모음의 지난 주에서 실패한 작업을 얻습니다.
From  매개 변수는 과거 7일의 시간을 UTC로 지정합니다.
이 명령은 To 매개 변수에 대한 값을 *지정하지* 않습니다.
따라서 현재 시간의 기본값을 사용하게 됩니다.

### 예제 3: 진행 중 작업 및 완료 대기
```
PS C:\> 
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

이 스크립트는 작업이 완료될 때까지 현재 진행 중인 첫 번째 작업을 폴링합니다.

## PARAMETERS

### -BackupManagementType
Backup 관리 유형을 지정합니다.
현재 AzureVM, AzureStorage만 지원됩니다.

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

### -From
이 cmdlet에서 얻을 작업의 시간 범위의 시작을 **DateTime** 개체로 지정합니다.
**DateTime 개체를** 얻습니다. Get-Date cmdlet을 사용합니다.
**DateTime** 개체에 대한 자세한 내용은 `Get-Help Get-Date` .를 입력합니다.
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

### -Job
얻을 Backup 작업의 이름을 지정합니다.

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
이 cmdlet이 얻을 작업의 ID를 지정합니다.
ID는 **AzureRmRecoveryServicesBackupJob** 개체의 InstanceId 속성입니다.
**AzureRmRecoveryServicesBackupJob** 개체를 얻습니다. Get-AzRecoveryServicesBackupJob을 사용합니다.

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

### -Operation
이 cmdlet에서 얻을 작업의 작업을 지정합니다.
이 매개 변수에 허용되는 값은
- Backup
- ConfigureBackup
- DeleteBackupData
- 등록
- 복원
- UnProtect
- 등록을 등록하지 않은 경우

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

### -Status
이 cmdlet이 얻을 작업의 상태를 지정합니다.
이 매개 변수에 허용되는 값은
- InProgress
- 실패
- Cancelled
- 취소
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
이 cmdlet에서 얻을 작업의 시간 범위의 끝을 **DateTime** 개체로 지정합니다.
기본값은 현재 시스템 시간입니다.
이 매개 변수를 지정하는 경우 From 매개 변수도 *지정해야* 합니다.
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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase

## 참고 사항

## 관련 링크


[Stop-AzRecoveryServicesBackupJob](./Stop-AzRecoveryServicesBackupJob.md)

[Wait-AzRecoveryServicesBackupJob](./Wait-AzRecoveryServicesBackupJob.md)


