---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 7ebbb3cf53c422a3a4d5c73f156cd3890eaa41e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491702"
---
# Get-AzRecoveryServicesBackupJobDetail

## SYNOPSIS

Backup 작업의 세부 정보를 얻습니다.

## 구문

### JobFilterSet(기본값)
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### IdFilterSet
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명

**Get-AzRecoveryServicesBackupJobDetail** cmdlet은 지정된 작업의 Azure Backup 작업 세부 정보를 얻습니다.
-VaultId 매개 변수를 사용하여 자격 증명 모음 컨텍스트를 설정합니다.

경고: **Get-AzRecoveryServicesBackupJobDetails** 별칭은 향후의 새로운 변경 릴리스에서 제거됩니다.

## 예제

### 예제 1: 실패한 작업의 Backup 작업 세부 정보 얻기

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

첫 번째 명령은 관련 자격 증명 모음을 페치합니다. 두 번째 명령은 자격 증명 모음에 실패한 작업의 배열을 구한 다음, $Jobs 저장합니다.
세 번째 명령은 실패한 첫 번째 작업의 작업 세부 정보를 $Jobs 다음 $JobDetails 변수에 저장합니다.
마지막 명령은 실패한 작업의 오류 세부 정보를 표시합니다.

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

얻을 작업을 지정합니다.
**BackupJob 개체를 얻습니다.** **Get-AzRecoveryServicesBackupJob** cmdlet을 사용합니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId

Backup 작업의 ID를 지정합니다.
ID는 **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** 개체의 JobId 속성입니다.

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases:

Required: True
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

### System.String

## 출력

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase

## 참고 사항

## 관련 링크

[Get-AzRecoveryServicesBackupJob](./Get-AzRecoveryServicesBackupJob.md)
