---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
ms.openlocfilehash: a977de2b4a60f0fc5ae93e175d521d398d40f850
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882966"
---
# Get-AzureRmApplicationGatewaySslPredefinedPolicy

## SYNOPSIS
응용 프로그램 게이트웨이에서 제공 하는 미리 정의 된 SSL 정책을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzureRmApplicationGatewaySslPredefinedPolicy** Cmdlet은 응용 프로그램 게이트웨이에서 제공 하는 미리 정의 된 SSL 정책을 가져옵니다.

## 예제의

### 예제 1
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

이 명령은 미리 정의 된 모든 SSL 정책을 반환 합니다.

### 예제 2
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

이 명령은 이름이 AppGwSslPolicy20170401 인 미리 정의 된 정책을 반환 합니다.

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
Ssl 미리 정의 된 정책 이름

```yaml
Type: String
Parameter Sets: (All)
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

### 않아야

## 출력

### PSApplicationGatewaySslPredefinedPolicy에 대 한.
4.1.0.0, PSApplicationGatewaySslPredefinedPolicy, Microsoft azure. Commands. 네트워크, 버전 =, Culture = 중립, PublicKeyToken = null]],. 컬렉션인 ' 1 [[Microsoft azure.]

## 상속자

## 관련 링크

