---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: afef81ad904ccd5bf53f0b2a09bb10511e71fca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536220"
---
# Get-AzureRmRecoveryServicesAsrJob

## SYNOPSIS
지정 된 ASR 작업 또는 복구 서비스 자격 증명 모음의 최근 ASR 작업 목록에 대 한 세부 정보를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByParam (기본값)
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [<CommonParameters>]
```

### ByName
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [<CommonParameters>]
```

### ByObject
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [<CommonParameters>]
```

## 설명은
**AzureRmRecoveryServicesAsrJob** Cmdlet은 Azure Site Recovery 작업을 가져옵니다.
이 cmdlet을 사용 하 여 복구 서비스 자격 증명 모음에서 ASR 작업을 볼 수 있습니다.

## 예제의

### 예제 1
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

특정 ASR 개체의 모든 작업을 반환 합니다 (복제 된 항목 또는 복구 계획과 같은 ASR 개체를 해당 ID로 참조). 

## 변수

### -EndTime
작업의 종료 시간을 지정 합니다.
이 cmdlet은 지정 된 시간 전에 시작 된 모든 작업을 가져옵니다.
이 매개 변수에 대 한 **DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.
자세한 내용은을 입력 `Get-Help Get-Date` 하세요.

```yaml
Type: DateTime
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
Type: ASRJob
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
Type: String
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
Type: DateTime
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
Type: String
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
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### SiteRecovery. r i m m 작업

## 출력

### System.webserver. t e r ' 1 [[SiteRecovery Rjob], [[Microsoft Azure. SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])

## 상속자

## 관련 링크

[다시 시작-AzureRmRecoveryServicesAsrJob](./Restart-AzureRmRecoveryServicesAsrJob.md)

[이력서-AzureRmRecoveryServicesAsrJob](./Resume-AzureRmRecoveryServicesAsrJob.md)

[중지-AzureRmRecoveryServicesAsrJob](./Stop-AzureRmRecoveryServicesAsrJob.md)
