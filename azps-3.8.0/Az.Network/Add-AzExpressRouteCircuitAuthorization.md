---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 047400472d3f42d5daff0f0ea6aed44455608eb3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034569"
---
# Add-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Express 경로 회로 인증을 추가 합니다.

## 구문과

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzExpressRouteCircuitAuthorization** Cmdlet은 express 경로 회로에 인증을 추가 합니다. Express 경로 회로는 공용 인터넷 대신 연결 공급자를 사용 하 여 온-프레미스 네트워크를 Microsoft 클라우드에 연결 합니다. Express 경로 회로의 소유자는 각 회로에 대해 최대 10 개의 권한을 만들 수 있습니다. 이러한 권한 부여는 가상 네트워크 소유자가 네트워크를 회로에 연결 하는 데 사용할 수 있는 인증 키를 생성 합니다 (가상 네트워크 당 하나의 권한 부여). **추가-AzExpressRouteCircuitAuthorization** 는 회로에 새 권한 부여를 추가 하 고 동시에 해당 하는 인증 키를 생성 합니다. 이러한 키는 언제 든 지 Get-AzExpressRouteCircuitAuthorization cmdlet을 실행 하 여 볼 수 있으며 필요한 경우 복사 하 여 적절 한 네트워크 소유자에 게 전달할 수 있습니다.
**Add-AzExpressRouteCircuitAuthorization** 을 실행 한 후에는 Set-AzExpressRouteCircuit cmdlet을 호출 하 여 키를 활성화 해야 합니다. **Set-AzExpressRouteCircuit** 를 호출 하지 않으면 권한 부여가 회로에 추가 되지만 사용할 수 있도록 설정 되지 않습니다.

## 예제의

### 예제 1: 지정 된 Express 경로 회로에 대 한 권한 부여 추가
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

이 예제의 명령은 기존 Express 경로에 새 인증을 추가 합니다. 첫 번째 명령은 **AzExpressRouteCircuit** 를 사용 하 여 ContosoCircuit 라는 회로에 대 한 개체 참조를 만듭니다. 해당 개체 참조는 $Circuit 라는 변수에 저장 됩니다.
두 번째 명령에서는 **추가-AzExpressRouteCircuitAuthorization** cmdlet을 사용 하 여 새 권한 부여 (ContosoCircuitAuthorization)를 express 회로에 추가 합니다. 이 명령은 권한 부여를 추가 하지만 해당 인증을 활성화 하지는 않습니다. 인증을 활성화 하려면 예제의 마지막 명령에 표시 된 **Set-AzExpressRouteCircuit** 가 필요 합니다.

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

### -ExpressRouteCircuit
이 cmdlet이 권한 부여를 추가 하는 대상 지정 회로를 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -이름
추가할 회로 승인의 이름을 지정 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSExpressRouteCircuit에 대 한.

## 출력

### PSExpressRouteCircuit에 대 한.

## 상속자

## 관련 링크

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[새로운 AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[제거-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
