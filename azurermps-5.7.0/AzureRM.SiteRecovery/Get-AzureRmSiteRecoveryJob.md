---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: dc8a1e6cfe8c3d68af0f8c413a0e96cac9feaee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531630"
---
# Get-AzureRmSiteRecoveryJob

## SYNOPSIS
현재 사이트 복구 자격 증명 모음에 대 한 작업 정보를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByParam (기본값)
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObject
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmSiteRecoveryJob** Cmdlet은 Azure Site Recovery 작업을 가져옵니다.
이 cmdlet을 사용 하 여 현재 사이트 복구 자격 증명 모음에 대 한 작업 정보를 볼 수 있습니다.

## 예제의

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
사이트 복구 작업을 지정 합니다.

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
작업을 식별 하는 고유한 이름을 지정 합니다.

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
사이트 복구 작업의 입력 상태를 지정 합니다.
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
작업을 대상으로 하는 개체의 ID를 지정 합니다.

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

### ASRJob
' Job ' 매개 변수는 파이프라인에서 ' ASRJob ' 형식의 값을 허용 합니다.

## 출력

### System.webserver. t e r ' 1 [SiteRecovery Rm 작업]

## 상속자

## 관련 링크

[다시 시작-AzureRmSiteRecoveryJob](./Restart-AzureRmSiteRecoveryJob.md)

[이력서-AzureRmSiteRecoveryJob](./Resume-AzureRmSiteRecoveryJob.md)

[중지-AzureRmSiteRecoveryJob](./Stop-AzureRmSiteRecoveryJob.md)
