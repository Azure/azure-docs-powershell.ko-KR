---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: c6db110c1657eb79deae3adcdfada8a835becdb6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700357"
---
# New-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Express 경로 회로 인증을 만듭니다.

## 구문과

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzExpressRouteCircuitAuthorization** Cmdlet은 express 경로 회로에 추가할 수 있는 회로 인증을 만듭니다. Express 경로 회로는 공용 인터넷 대신 연결 공급자를 사용 하 여 온-프레미스 네트워크를 Microsoft 클라우드에 연결 합니다. Express 경로 회로의 소유자는 각 회로에 대해 최대 10 개의 권한을 만들 수 있습니다. 이러한 권한 부여는 가상 네트워크 소유자가 네트워크를 회로에 연결 하는 데 사용할 수 있는 인증 키를 생성 합니다. 각 가상 네트워크에는 하나의 권한 부여만 가능 합니다.
Express 경로를 만든 후에 **추가-AzExpressRouteCircuitAuthorization** 를 사용 하 여 해당 회로에 대 한 인증을 추가할 수 있습니다.
또는 **새 AzExpressRouteCircuitAuthorization** 를 사용 하 여 회로가 생성 될 때 새 회로에 추가할 수 있는 인증을 만들 수 있습니다.

## 예제의

### 예제 1: 새 회로 승인 만들기
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

이 명령은 ContosoCircuitAuthorization 이라는 새 회로 인증을 만든 다음 해당 개체를 $Authorization 라는 변수에 저장 합니다. 개체를 변수에 저장 하는 것이 중요 합니다. 하지만 **새 AzExpressRouteCircuitAuthorization** 는 회로 인증을 만들 수 있지만, 회로 경로에는 해당 권한을 추가할 수 없습니다. 대신 새 Express 경로를 만들 때 변수 $Authorization를 사용 New-AzExpressRouteCircuit.
자세한 내용은 New-AzExpressRouteCircuit cmdlet에 대 한 설명서를 참조 하세요.

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

### -이름
새 Express 경로 회로 권한 부여에 대 한 고유한 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
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

### 않아야

## 출력

### PSExpressRouteCircuitAuthorization에 대 한.

## 상속자

## 관련 링크

[추가-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[제거-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

