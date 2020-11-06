---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: d79a717fcf5d2422f86df4184d9c0344ebc32d28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536215"
---
# Get-AzureRmRecoveryServicesAsrStorageClassification

## SYNOPSIS
복구 서비스 자격 증명 모음에서 사용 가능한 (검색 된) ASR 저장소 분류를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByFabricObject (기본값)
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [<CommonParameters>]
```

### ByObjectWithName
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### ByObjectWithFriendlyName
```
Get-AzureRmRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## 설명은
**AzureRmRecoveryServicesAsrStorageClassification** Cmdlet은 복구 서비스 자격 증명 모음에 있는 검색 된 ASR 저장소 분류의 세부 정보를 가져옵니다.

## 예제의

### 예제 1
```
PS C:\> $StorageClassifications = Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

지정 된 ASR 패브릭에 해당 하는 검색 된 저장소 분류를 나열 합니다. 

## 변수

### -패브릭
ASR fabric 개체를 지정 합니다. Cmdlet은 지정 된 ASR 패브릭에 해당 하는 검색 된 저장소 분류의 세부 정보를 가져옵니다. 

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -FriendlyName
가져올 저장소 분류 개체의 친근 한 이름을 지정 합니다.

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
가져올 저장소 분류 개체의 이름을 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### SiteRecovery. r m m a m

## 출력

### System.webserver. t e 1 [[SiteRecovery] [[Microsoft Azure. ASRStorageClassification, SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])

## 상속자

## 관련 링크

