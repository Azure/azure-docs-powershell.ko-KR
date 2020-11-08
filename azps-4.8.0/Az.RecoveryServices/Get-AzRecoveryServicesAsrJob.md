---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: a367fd8643dc29901f8dfafdbecd59a8386320a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047702"
---
# Get-AzRecoveryServicesAsrJob

## SYNOPSIS
지정 된 ASR 작업 또는 복구 서비스 자격 증명 모음의 최근 ASR 작업 목록에 대 한 세부 정보를 가져옵니다.

## 구문과

### ByParam (기본값)
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

## 설명은
**AzRecoveryServicesAsrJob** Cmdlet은 Azure Site Recovery 작업을 가져옵니다.
이 cmdlet을 사용 하 여 복구 서비스 자격 증명 모음에서 ASR 작업을 볼 수 있습니다.

## 예제의

### 예제 1
```powershell
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

특정 ASR 개체의 모든 작업을 반환 합니다 (복제 된 항목 또는 복구 계획과 같은 ASR 개체를 해당 ID로 참조). 

### 예제 2

지정 된 ASR 작업 또는 복구 서비스 자격 증명 모음의 최근 ASR 작업 목록에 대 한 세부 정보를 가져옵니다. 생성

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesAsrJob -Job $Job
```

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

### -EndTime
작업의 종료 시간을 지정 합니다.
이 cmdlet은 지정 된 시간 전에 시작 된 모든 작업을 가져옵니다.
이 매개 변수에 대 한 **DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.
자세한 내용은을 입력 `Get-Help Get-Date` 하세요.

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

### -작업
업데이트 세부 정보를 얻을 ASR 작업 개체를 지정 합니다.

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

### -이름
이름으로 ASR 작업을 지정 합니다.

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
작업의 시작 시간을 지정 합니다.
이 cmdlet은 지정 된 시간 이후에 시작 된 모든 작업을 가져옵니다.

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

### -상태
ASR 작업의 상태를 지정 합니다.
이 cmdlet은 지정 된 상태와 일치 하는 모든 작업을 가져옵니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- NotStarted
- InProgress
- 했음을
- 나머지
- 못함
- 되었습니다
- 된

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
개체의 ID를 지정 합니다. 지정 된 개체에 대 한 작업을 검색 하는 데 사용 됩니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### SiteRecovery. r i m m 작업

## 출력

### SiteRecovery. r i m m 작업

## 상속자

## 관련 링크

[다시 시작-AzRecoveryServicesAsrJob](./Restart-AzRecoveryServicesAsrJob.md)

[이력서-AzRecoveryServicesAsrJob](./Resume-AzRecoveryServicesAsrJob.md)

[중지-AzRecoveryServicesAsrJob](./Stop-AzRecoveryServicesAsrJob.md)
