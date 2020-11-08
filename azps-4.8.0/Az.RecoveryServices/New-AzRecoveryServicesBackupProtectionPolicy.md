---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 0a60e3bd7f07f69687766b95eb3d56be3ef1d56f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214260"
---
# New-AzRecoveryServicesBackupProtectionPolicy

## SYNOPSIS
백업 보호 정책을 만듭니다.

## 구문과

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzRecoveryServicesBackupProtectionPolicy** cmdlet은 자격 증명 모음에 백업 보호 정책을 만듭니다.
보호 정책은 하나 이상의 보존 정책에 연결 됩니다.
보존 정책은 복구 지점이 Azure Backup으로 유지 되는 기간을 정의 합니다.
Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet을 사용 하 여 기본 보존 정책을 가져올 수 있습니다.
Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet을 사용 하 여 기본 일정 정책을 가져올 수 있습니다.
**SchedulePolicy** 및 **보존 정책** 개체는 **새로운 AzRecoveryServicesBackupProtectionPolicy** cmdlet에 대 한 입력으로 사용 됩니다.
현재 cmdlet을 사용 하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.

## 예제의

### 예제 1: 백업 보호 정책 만들기
```powershell
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

첫 번째 명령은 기본 **SchedulePolicyObject** 를 가져온 다음이를 $SchPol 변수에 저장 합니다.
두 번째 명령은 $SchPol의 일정 정책에서 예약 된 모든 실행 시간을 제거 합니다.
세 번째 명령은 Get-Date cmdlet을 사용 하 여 현재 날짜와 시간을 가져옵니다.
네 번째 명령은 예약 된 실행 시간에 $Dt의 현재 날짜 및 시간을 일정 정책에 추가 합니다.
다섯 번째 명령은 기본 **보존 정책** 개체를 가져온 다음 $RetPol 변수에 저장 합니다.
여섯 번째 명령은 보존 기간 정책을 365 days로 설정 합니다.
마지막 명령은 이전 명령으로 만든 일정 및 보존 정책에 따라 **BackupProtectionPolicy** 개체를 만듭니다.

### 예제 2

백업 보호 정책을 만듭니다. 생성

```powershell <!-- Aladdin Generated Example --> 
New-AzRecoveryServicesBackupProtectionPolicy -Name 'NewPolicy' -RetentionPolicy $RetPol -SchedulePolicy $SchPol -VaultId $vault.ID -WorkloadType AzureVM
```

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
Position: 3
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

### -이름
정책의 이름을 지정 합니다.

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

### -보존 정책
기본 **보존 정책** 개체를 지정 합니다.
Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet을 사용 하 여 **보존 정책** 개체를 가져올 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SchedulePolicy
기본 **SchedulePolicy** 개체를 지정 합니다.
Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet을 사용 하 여 **SchedulePolicy** 개체를 가져올 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.

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

### WorkloadType에서. i. i m/.

### 시스템 Null 허용 ' 1 [[Microsoft Azure. e-유틸리티]. system.webserver 관리 형식, Microsoft Azure. PowerShell, 버전 = 1.0.0.0, Culture = 중립, PublicKeyToken = null]])

### Microsoft Azure.. i 0. a 0 유틸리티.

### SchedulePolicyBase에서. i. i m/.

### System. 문자열

## 출력

### Microsoft. *. i i m.. i i m.

## 상속자

## 관련 링크

[Enable-AzRecoveryServicesBackupProtection](./Enable-AzRecoveryServicesBackupProtection.md)

[Get-AzRecoveryServicesBackupProtectionPolicy](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[Get-AzRecoveryServicesBackupRetentionPolicyObject](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[Get-AzRecoveryServicesBackupSchedulePolicyObject](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[제거-AzRecoveryServicesBackupProtectionPolicy](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[Set-AzRecoveryServicesBackupProtectionPolicy](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


