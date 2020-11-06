---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
ms.openlocfilehash: 27d27cf3df8c41eaa507d9223c73f2b36637a04c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526040"
---
# Get-AzureRmSecurityPricing

## SYNOPSIS
범위에 대 한 Azure 보안 센터에 대 한 가격 책정 계층 데이터를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### 구독 범위 (기본값)
```
Get-AzureRmSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelResource
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### 구독 Levelresource
```
Get-AzureRmSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 리소스
```
Get-AzureRmSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
Azure 보안 센터 가격 책정 계층은 범위 별로 결정 되며이 cmdlet을 사용 하 여 구성 된 가격 책정 계층을 가져올 수 있습니다.
구독 가격 책정 계층에는 모든 리소스 그룹이 포함 됩니다.
자원 그룹 가격 책정 계층이 구독 가격 책정 계층을 재정의 합니다.

## 예제의

### 예제 1
```powershell
PS C:\> Get-AzureRmSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

구독에 대해 구성 된 모든 가격 책정 계층과 그 아래의 리소스 그룹을 가져옵니다.

### 예제 2
```powershell
PS C:\> Get-AzureRmSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

"MyService1" 리소스 gorup에 대해 구성 된 가격 책정 계층을 가져옵니다.

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
리소스 이름입니다.

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
리소스 ID입니다.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### Pricings. PSSecurityPricing에 대 한 Microsoft

## 상속자

## 관련 링크
