---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360753"
---
# Remove-AzExpressRouteCircuitAuthorization

## SYNOPSIS
기존 ExpressRoute 구성 권한 부여를 제거합니다.

## 구문

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Remove-AzExpressRouteCircuitAuthorization** cmdlet은 ExpressRoute 회로에 할당된 권한 부여를 제거합니다. ExpressRoute 회로는 공용 인터넷 대신 연결 공급자를 사용하여 Azure에 Azure에 연결합니다. ExpressRoute 회로의 소유자는 각 회로에 대해 10개까지 권한 부여를 만들 수 있습니다. 이러한 권한 부여는 가상 네트워크 소유자가 자신의 네트워크를 회로에 연결하는 데 사용할 수 있는 권한 부여 키를 생성합니다. 가상 네트워크당 하나의 권한 부여만 있을 수 있습니다. 그러나 회로 소유자는 **제거-AzExpressRouteCircuitAuthorization을** 사용하여 가상 네트워크에 할당된 권한 부여를 제거할 수 있습니다. 이 경우 해당 가상 네트워크는 더 이상 ExpressRoute 회로를 사용하여 Azure에 연결할 수 없습니다.

## 예제

### 예제 1: ExpressRoute 회로에서 회로 권한 부여 제거
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

이 예제에서는 ExpressRoute 회로에서 회로 권한 부여를 제거합니다. 첫 번째 명령은 **Get-AzExpressRouteCircuit** cmdlet을 사용하여 ContosoCircuit이라는 ExpressRoute 회로에 대한 개체 참조를 만들고 결과를 이름 지정 변수에 $Circuit.
두 번째 명령은 제거를 위해 회로 권한 부여 ContosoCircuitAuthorization을 표시합니다.
세 번째 명령은 Set-AzExpressRouteCircuit cmdlet을 사용하여 $Circuit 변수에 저장된 ExpressRoute 회로의 제거를 확인할 수 있습니다.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
이 cmdlet에서 제거하는 ExpressRouteCircuit 개체를 지정합니다.

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
이 cmdlet이 제거하는 회로 권한 부여의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## 출력

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## 참고 사항

## 관련 링크

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
