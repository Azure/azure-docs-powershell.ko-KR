---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 5bf91aafffb1c6fd650b5fd88f343897afc6c5d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979435"
---
# Get-AzRecoveryServicesBackupSchedulePolicyObject

## SYNOPSIS
기본 일정 정책 개체를 얻습니다.

## 구문

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet은 기본 **AzureRMRecoveryServicesSchedulePolicyObject** 를 얻습니다.
이 개체는 시스템에 유지되지 않습니다.
새 백업 보호 정책을 만들기 위해 New-AzRecoveryServicesBackupProtectionPolicy cmdlet과 함께 조작하고 사용할 수 있는 임시 개체입니다.

## 예제

### 예제 1: 일정 빈도를 매주로 설정
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

첫 번째 명령은 보존 정책 개체를 구한 다음, $RetPol 변수에 저장합니다.
두 번째 명령은 일정 정책 개체를 얻은 다음, $SchPol 변수에 저장합니다.
세 번째 명령은 일정 정책의 빈도를 매주 변경합니다.
마지막 명령은 업데이트된 일정을 사용하여 백업 보호 정책을 만듭니다.

### 예제 2: 백업 시간 설정
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

첫 번째 명령은 일정 정책 개체를 얻은 다음, $SchPol 변수에 저장합니다.
두 번째 명령은 예약된 모든 실행 시간을 $SchPol.
세 번째 명령은 현재 날짜와 시간을 얻은 다음, $DT 변수에 저장합니다.
네 번째 명령은 예약된 실행 시간을 현재 시간으로 바 대체합니다.
AzureVM을 하루 한 번만 백업할 수 있으므로 백업 시간을 다시 설정하려면 원래 일정을 바야 합니다.
마지막 명령은 새 일정을 사용하여 백업 보호 정책을 만듭니다.

## 매개 변수

### -BackupManagementType
보호되는 리소스의 클래스입니다. 이 매개 변수에 대해 허용되는 값은 다음입니다.
- AzureVM 
- AzureStorage
- AzureWorkload

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
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

### -WorkloadType
리소스의 워크로드 유형입니다. 이 매개 변수에 대해 허용되는 값은 다음입니다.
- AzureVM 
- AzureFiles
- MSSQL


```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase

## 참고 사항

## 관련 링크

[New-AzRecoveryServicesBackupProtectionPolicy](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[Set-AzRecoveryServicesBackupProtectionPolicy](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


