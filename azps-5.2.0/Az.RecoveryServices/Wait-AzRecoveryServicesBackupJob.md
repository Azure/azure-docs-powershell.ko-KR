---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: d494169c989096ce562858c500289527479d42dd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329661"
---
# Wait-AzRecoveryServicesBackupJob

## SYNOPSIS

Backup 작업이 완료될 때까지 기다릴 수 있습니다.

## 구문

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명

**Wait-AzRecoveryServicesBackupJob** cmdlet은 Azure Backup 작업이 완료될 때까지 대기합니다.
백업 작업은 시간이 오래 걸릴 수 있습니다.
스크립트의 일부로 백업 작업을 실행하면 스크립트가 작업을 완료할 때까지 기다렸다가 다른 태스크로 계속 진행할 수 있습니다.
이 cmdlet을 포함하는 스크립트는 작업 상태에 대한 Backup 서비스를 폴링하는 스크립트보다 간단할 수 있습니다.
-VaultId 매개 변수를 사용하여 자격 증명 모음 컨텍스트를 설정합니다.

## 예제

### 예제 1: 작업이 완료될 때까지 대기

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

이 스크립트는 작업이 완료되거나 1시간의 시간 제한 기간이 만료될 때까지 현재 진행 중인 첫 번째 작업을 폴링합니다.

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

### -Job

대기할 작업을 지정합니다.
**BackupJob 개체를 얻습니다.** **Get-AzRecoveryServicesBackupJob** cmdlet을 사용합니다.

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Timeout

이 cmdlet이 작업이 완료될 때까지 대기하는 최대 시간(초)을 지정합니다.
시간 시간 값을 지정하는 것이 좋습니다.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.Object

### System.String

## 출력

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase

## 참고 사항

## 관련 링크

[Get-AzRecoveryServicesBackupJob](./Get-AzRecoveryServicesBackupJob.md)
