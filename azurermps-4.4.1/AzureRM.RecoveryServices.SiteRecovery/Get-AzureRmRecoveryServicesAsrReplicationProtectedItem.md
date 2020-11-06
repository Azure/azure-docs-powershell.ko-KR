---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: fbd2f518d3bdcf64599e32b55cdb9f416c29be21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537020"
---
# Get-AzureRmRecoveryServicesAsrReplicationProtectedItem

## SYNOPSIS
Azure Site Recovery 복제 보호 항목의 속성을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByObject (기본값)
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### ByObjectWithName
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

### ByObjectWithFriendlyName
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

### ByProtectableItemObject
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [<CommonParameters>]
```

## 설명은
**AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet은 지정 된 asr 보호 컨테이너에서 모든 또는 지정 된 asr 복제 보호 항목의 속성을 가져옵니다.

## 예제의

### 예제 1
```
PS C:\> $ReplicationProtectedItems = Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

지정 된 ASR 보호 컨테이너에서 모든 복제 보호 항목을 나열 합니다.

## 변수

### -FriendlyName
가져올 복제 보호 항목의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
가져올 복제 보호 항목의 이름을 지정 합니다.

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

### -ProtectableItem
ASR 보호 가능한 항목 개체를 지정 합니다. Cmdlet은 항목이 보호 되는 경우 지정 된 ASR 보호 가능한 항목에 해당 하는 ASR 복제 보호 항목을 가져옵니다.

```yaml
Type: ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ProtectionContainer
복제 보호 항목에 해당 하는 ASR 보호 컨테이너의 ASR 보호 컨테이너 개체를 지정 합니다. 

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
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

### SiteRecovery. ASRProtectionContainer에 대 한 서비스
SiteRecovery. ASRProtectableItem에 대 한 서비스

## 출력

### System.webserver. t e 1 [[SiteRecovery] [[Microsoft Azure. ASRReplicationProtectedItem, SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])

## 상속자

## 관련 링크

[새로운 AzureRmRecoveryServicesAsrReplicationProtectedItem](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[제거-AzureRmRecoveryServicesAsrReplicationProtectedItem](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[Set-AzureRmRecoveryServicesAsrReplicationProtectedItem](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
