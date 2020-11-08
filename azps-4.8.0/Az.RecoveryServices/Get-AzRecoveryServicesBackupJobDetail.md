---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 7ebbb3cf53c422a3a4d5c73f156cd3890eaa41e5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056095"
---
# Get-AzRecoveryServicesBackupJobDetail

## SYNOPSIS

백업 작업에 대 한 세부 정보를 가져옵니다.

## 구문과

### JobFilterSet (기본값)
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### IdFilterSet
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은

**AzRecoveryServicesBackupJobDetail** cmdlet은 지정 된 작업에 대 한 Azure 백업 작업 세부 정보를 가져옵니다.
-VaultId 매개 변수를 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.

경고: **AzRecoveryServicesBackupJobDetails** alias는 향후 주요 변경 릴리스에서 제거 됩니다.

## 예제의

### 예제 1: 실패 한 작업에 대 한 백업 작업 세부 정보 가져오기

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

첫 번째 명령은 관련 자격 증명 모음을 페치합니다. 두 번째 명령은 자격 증명 모음에서 실패 한 작업 배열을 가져온 다음 $Jobs 배열에 저장 합니다.
세 번째 명령은 $Jobs의 첫 번째 실패 한 작업에 대 한 작업 세부 정보를 가져온 다음 $JobDetails 변수에 저장 합니다.
마지막 명령은 실패 한 작업에 대 한 오류 세부 정보를 표시 합니다.

## 변수

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

### -작업

가져올 작업을 지정 합니다.
**Backupjob** 개체를 가져오려면 **AzRecoveryServicesBackupJob** cmdlet을 사용 합니다.

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

백업 작업의 ID를 지정 합니다.
이 ID는 **Microsoft Azure.** . d m.-To-Commands 기본 개체의 JobId 속성입니다.

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

[Get-AzRecoveryServicesBackupJob](./Get-AzRecoveryServicesBackupJob.md)
