---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 96a30621bc545b635262fd7937e0e55739d0be7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537023"
---
# Get-AzureRmRecoveryServicesAsrRecoveryPoint

## SYNOPSIS
복제 보호 항목에 대해 사용 가능한 복구 지점을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByObject (기본값)
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [<CommonParameters>]
```

### ByObjectWithName
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -Name <String>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [<CommonParameters>]
```

## 설명은
**AzureRmRecoveryServicesAsrRecoveryPoint** cmdlet은 복제 보호 항목에 대해 사용 가능한 복구 지점 목록을 가져옵니다.

## 예제의

### 예제 1
```
PS C:\> $RecoveryPoints = Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

지정 된 ASR 복제 보호 항목에 대 한 복구 지점을 가져옵니다.

## 변수

### -이름
가져올 복구 지점의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationProtectedItem
사용 가능한 복구 지점 목록을 가져올 Azure Site Recovery 복제 보호 항목 개체를 지정 합니다.

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스

## 출력

### System.webserver. t e 1 [[SiteRecovery] [[Microsoft Azure. ASRRecoveryPoint, SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])

## 상속자

## 관련 링크

[편집-AzureRmRecoveryServicesAsrRecoveryPlan](./Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[Get-AzureRmRecoveryServicesAsrRecoveryPlan](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[새로운 AzureRmRecoveryServicesAsrRecoveryPlan](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[제거-AzureRmRecoveryServicesAsrRecoveryPlan](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[업데이트-AzureRmRecoveryServicesAsrRecoveryPlan](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
