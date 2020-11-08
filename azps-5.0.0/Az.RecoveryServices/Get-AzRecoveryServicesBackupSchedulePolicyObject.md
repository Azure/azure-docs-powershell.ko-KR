---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: d66b8515c6b2c3782c6f6c2b49d462dbb7bd1660
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215707"
---
# Get-AzRecoveryServicesBackupSchedulePolicyObject

## SYNOPSIS
기본 일정 정책 개체를 가져옵니다.

## 구문과

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzRecoveryServicesBackupSchedulePolicyObject** cmdlet은 기본 **AzureRMRecoveryServicesSchedulePolicyObject** 를 가져옵니다.
이 개체는 시스템에 유지 되지 않습니다.
새 백업 보호 정책을 만들기 위해 New-AzRecoveryServicesBackupProtectionPolicy cmdlet을 조작 하 고 사용할 수 있는 임시 개체입니다.

## 예제의

### 예제 1: 일정 주기를 매주로 설정
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

첫 번째 명령은 보존 정책 개체를 가져온 다음 $RetPol 변수에 저장 합니다.
두 번째 명령은 일정 정책 개체를 가져온 다음 $SchPol 변수에 저장 합니다.
세 번째 명령은 일정 정책의 빈도를 매주로 변경 합니다.
마지막 명령은 업데이트 된 일정으로 백업 보호 정책을 만듭니다.

### 예제 2: 백업 시간 설정
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

첫 번째 명령은 일정 정책 개체를 가져온 다음 $SchPol 변수에 저장 합니다.
두 번째 명령은 $SchPol에서 예약 된 모든 실행 시간을 제거 합니다.
세 번째 명령은 현재 날짜와 시간을 가져온 다음이를 $DT 변수에 저장 합니다.
네 번째 명령은 예약 된 실행 시간을 현재 시간으로 바꿉니다.
1 일에 한 명만을 한 번만 백업할 수 있으므로 백업 시간을 다시 설정 하려면 원래 일정을 바꿔야 합니다.
마지막 명령은 새 일정을 사용 하 여 백업 보호 정책을 만듭니다.

## 변수

### -BackupManagementType
보호 되는 리소스의 클래스입니다. 이 매개 변수에 허용 되는 값은 다음과 같습니다.
- Add-azurevm 
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

### -WorkloadType
리소스의 작업 부하 유형입니다. 이 매개 변수에 허용 되는 값은 다음과 같습니다.
- Add-azurevm 
- AzureFiles
- 원인은


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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### 않아야

## 출력

### SchedulePolicyBase에서. i. i m/.

## 상속자

## 관련 링크

[새로운 AzRecoveryServicesBackupProtectionPolicy](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[Set-AzRecoveryServicesBackupProtectionPolicy](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


