---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 9812316b20db927dea9bfe999cad54fe002bfc93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952304"
---
# Add-AzExpressRouteCircuitAuthorization

## SYNOPSIS
ExpressRoute 회로 권한 부여를 추가합니다.

## 구문

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Add-AzExpressRouteCircuitAuthorization** cmdlet은 ExpressRoute 회로에 권한 부여를 추가합니다. ExpressRoute 회로는 공용 인터넷 대신 연결 공급자를 사용하여 Microsoft 클라우드에 프레미스 네트워크를 연결합니다. ExpressRoute 회로의 소유자는 각 회로에 대해 10개까지 권한 부여를 만들 수 있습니다. 이러한 권한 부여는 가상 네트워크 소유자가 회로에 연결하는 데 사용할 수 있는 권한 부여 키를 생성합니다(가상 네트워크당 하나의 권한 부여). **Add-AzExpressRouteCircuitAuthorization은** 회로에 새 권한 부여를 추가하고 동시에 해당 권한 부여 키를 생성합니다. 이러한 키는 Get-AzExpressRouteCircuitAuthorization cmdlet을 실행하여 볼 수 있으며, 필요한 경우 해당 네트워크 소유자에게 복사하여 전달할 수 있습니다.
**Add-AzExpressRouteCircuitAuthorization을** 실행한 후 키를 활성화하려면 Set-AzExpressRouteCircuit cmdlet을 호출해야 합니다. **Set-AzExpressRouteCircuit를** 호출하지 않는 경우 권한 부여가 회로에 추가되지만 사용할 수 없습니다.

## 예제

### 예제 1: 지정된 ExpressRoute 회로에 권한 부여 추가
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

이 예제의 명령은 기존 ExpressRoute 회로에 새 권한 부여를 추가합니다. 첫 번째 명령은 **Get-AzExpressRouteCircuit를** 사용하여 ContosoCircuit라는 회로에 대한 개체 참조를 만듭니다. 해당 개체 참조는 이라는 변수에 $Circuit.
두 번째 명령에서는 **Add-AzExpressRouteCircuitAuthorization** cmdlet을 사용하여 ExpressRoute 회로에 새 권한 부여(ContosoCircuitAuthorization)를 추가합니다. 이 명령은 권한 부여를 추가하지만 해당 권한 부여를 활성화하지 않습니다. 권한 부여를 활성화하려면 예제의 최종 명령에 표시된 **Set-AzExpressRouteCircuit가** 필요합니다.

## 매개 변수

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
이 cmdlet이 권한 부여를 추가하는 ExpressRoute 회로를 지정합니다.

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

### -Name
추가할 회로 권한 부여의 이름을 지정합니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## 출력

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## 참고 사항

## 관련 링크

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
