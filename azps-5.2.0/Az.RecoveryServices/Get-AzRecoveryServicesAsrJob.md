---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: a367fd8643dc29901f8dfafdbecd59a8386320a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335889"
---
# Get-AzRecoveryServicesAsrJob

## SYNOPSIS
지정된 ASR 작업의 세부 정보 또는 Recovery Services 자격 증명 모음의 최근 ASR 작업 목록을 얻습니다.

## 구문

### ByParam(기본값)
```
Get-AzRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObject
```
Get-AzRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzRecoveryServicesAsrJob** cmdlet은 Azure Site Recovery 작업을 얻습니다.
이 cmdlet을 사용하여 Recovery Services 자격 증명 모음에서 ASR 작업을 볼 수 있습니다.

## 예제

### 예제 1
```powershell
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

특정 ASR 개체의 모든 작업을 반환합니다(ID별로 복제된 항목 또는 복구 계획과 같은 ASR 개체 참조). 

### 예제 2

지정된 ASR 작업의 세부 정보 또는 Recovery Services 자격 증명 모음의 최근 ASR 작업 목록을 얻습니다. (자동Generated)

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesAsrJob -Job $Job
```

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

### -EndTime
작업의 종료 시간을 지정합니다.
이 cmdlet은 지정된 시간 전에 시작된 모든 작업을 얻습니다.
이 매개 변수에 **대한 DateTime** 개체를 얻습니다. Get-Date cmdlet을 사용합니다.
자세한 내용은 `Get-Help Get-Date` .를 입력합니다.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
업데이트된 세부 정보를 얻을 ASR 작업 개체를 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
이름으로 ASR 작업을 지정합니다.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
작업의 시작 시간을 지정합니다.
이 cmdlet은 지정된 시간 후에 시작된 모든 작업을 얻습니다.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State
ASR 작업의 상태를 지정합니다.
이 cmdlet은 지정된 상태와 일치하는 모든 작업을 얻습니다.
이 매개 변수에 허용되는 값은

- NotStarted
- InProgress
- 성공
- 기타
- 실패
- Cancelled
- 일시 중단

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetObjectId
개체의 ID를 지정합니다. 지정된 개체에서 작업을 검색하는 데 사용됩니다.

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob

## 출력

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob

## 참고 사항

## 관련 링크

[Restart-AzRecoveryServicesAsrJob](./Restart-AzRecoveryServicesAsrJob.md)

[Resume-AzRecoveryServicesAsrJob](./Resume-AzRecoveryServicesAsrJob.md)

[Stop-AzRecoveryServicesAsrJob](./Stop-AzRecoveryServicesAsrJob.md)
