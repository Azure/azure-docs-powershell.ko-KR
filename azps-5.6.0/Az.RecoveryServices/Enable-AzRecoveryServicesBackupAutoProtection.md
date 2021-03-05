---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 81fa8a4ada2f2479d9aa2ecceb1de3c05c3f34c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005851"
---
# Enable-AzRecoveryServicesBackupAutoProtection

## SYNOPSIS
**Enable-AzRecoveryServicesBackupAutoProtection** cmdlet은 제공된 정책으로 주어진 인스턴스 내의 현재 및 향후 SQL DB의 자동 보호를 설정합니다.

## 구문

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
이 명령을 사용하면 사용자가 보호되지 않은 모든 DB 및 나중에 SQL 추가될 모든 DB를 자동으로 보호할 수 있습니다.  명령은 향후 모든 DB를 백업하는 것이기 때문에 작업이 SQLInstance 수준에서 수행되고 Azure Backup 서비스는 자동으로 보호되는 모든 새 DB에 대해 자동으로 보호되는 컨테이너를 정기적으로 검색합니다.

## 예제

### 예제 1
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultSQLPolicy"
PS C:\> $SQLInstance = Get-AzRecoveryServicesBackupProtectableItem -workloadType MSSQL -ItemType SQLInstance -VaultId $targetVault.ID -Name "MSSQLInstance" -ServerName "TestSQLServer" 
PS C:\> Enable-AzRecoveryServicesBackupAutoProtection -InputItem $SQLInstance -BackupManagementType AzureWorkload -WorkloadType MSSQL -Policy $Pol -VaultId $targetvault.ID 
```

첫 번째 cmdlet은 기본 정책 개체를 얻은 다음, $Pol 변수에 저장합니다.
두 번째 cmdlet은 보호 가능한 항목인 관련 SQLInstance를 페치합니다. 그런 다음 3번째 명령은 이 인스턴스의 정책을 사용하여 이 인스턴스에 대한 자동 보호를 $Pol.

### 예제 2

이 명령을 사용하면 사용자가 보호되지 않은 모든 기존 DB 및 나중에 주어진 정책으로 추가될 모든 DB를 자동으로 보호할 수 있습니다. (자동 재생)

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType AzureVM -InputItem <ProtectableItemBase> -Policy $Pol -VaultId $vault.ID -WorkloadType AzureVM
```

## 매개 변수

### -BackupManagementType
보호되는 리소스의 클래스입니다. 현재 이 cmdlet에 대해 지원되는 값은 MAB, AzureWorkload, AzureVM입니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
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

### -InputItem
입력으로 전달할 수 있는 보호 가능한 항목 개체를 지정합니다. 현재 지원되는 값은 "SQLInstance"형식의 보호 가능한Item 개체입니다. 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
자동 보호에 대한 결과를 반환합니다.

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

### -Policy
보호 정책 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
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

### -WorkloadType
리소스의 워크로드 유형입니다. 현재 지원되는 값은 AzureVM, WindowsServer, MSSQL입니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.


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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

## 출력

### System.Object

## 참고 사항

## 관련 링크
