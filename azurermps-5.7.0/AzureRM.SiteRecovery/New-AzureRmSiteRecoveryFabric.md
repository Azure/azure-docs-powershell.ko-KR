---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B087194B-DA3F-4E45-BD2D-788F9E6F03EA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 38a7f8ee32f02db10dc971d5be2016d5dea0b538
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524927"
---
# New-AzureRmSiteRecoveryFabric

## SYNOPSIS
Azure Site Recovery 패브릭을 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureRmSiteRecoveryFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzureRmSiteRecoveryFabric** cmdlet은 지정 된 형식의 Azure Site Recovery Fabric을 만듭니다.

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

### -이름
Azure Site Recovery 패브릭의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
Azure Site Recovery 패브릭 유형을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### SiteRecovery. r m m 작업

## 상속자

## 관련 링크

[Get-AzureRmSiteRecoveryFabric](./Get-AzureRmSiteRecoveryFabric.md)

[제거-AzureRmSiteRecoveryFabric](./Remove-AzureRmSiteRecoveryFabric.md)
