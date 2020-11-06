---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 84a50782e9906271e3943c8cd545780457a1adfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537024"
---
# Get-AzureRmRecoveryServicesAsrProtectionContainer

## SYNOPSIS
복구 서비스 자격 증명 모음에서 ASR 보호 컨테이너를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByFabricObject (기본값)
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [<CommonParameters>]
```

### ByObjectWithName
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### ByObjectWithFriendlyName
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## 설명은
**AzureRmRecoveryServicesAsrProtectionContainer** Cmdlet은 Recovery Services 자격 증명 모음에서 Azure Site Recovery 보호 컨테이너를 가져옵니다.
보호 컨테이너는 가상 컴퓨터와 같은 보호 되는 (검색 된) 개체를 위한 논리적 컨테이너 이며,
복제 정책은 보호 된 항목에 대 한 복제 설정을 정의 하 고 보호 컨테이너에 연결 하 고 보호 가능한 항목에 적용할 수 있습니다.

## 예제의

### 예제 1
```
PS C:\> $ProtectionContainers = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrProtectionContainer
```

지정 된 ASR 패브릭의 모든 ASR 보호 컨테이너 (위의 예제에서 파이프라인 입력)를 가져옵니다.

## 변수

### -패브릭
지정 된 ASR 패브릭에서 보호 컨테이너를 찾습니다.

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
찾을 ASR 보호 컨테이너의 이름을 지정 합니다.

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
찾을 ASR 보호 컨테이너의 이름을 지정 합니다.

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

### System.webserver. t e 1 [[SiteRecovery] [[Microsoft Azure. ASRProtectionContainer, SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])

## 상속자

## 관련 링크

