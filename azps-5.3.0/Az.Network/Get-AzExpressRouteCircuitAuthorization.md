---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 7c942968439d7d55fe78a3dd95c36501a2eaf10f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489959"
---
# Get-AzExpressRouteCircuitAuthorization

## SYNOPSIS
ExpressRoute 회로 권한 부여에 대한 정보를 얻습니다.

## 구문

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzExpressRouteCircuitAuthorization** cmdlet은 ExpressRoute 회로에 할당된 권한 부여에 대한 정보를 얻습니다. ExpressRoute 회로는 공용 인터넷 대신 연결 공급자를 사용하여 Microsoft 클라우드에 연결합니다. ExpressRoute 회로의 소유자는 각 회로에 대해 10개까지 권한 부여를 만들 수 있습니다. 이러한 권한 부여는 가상 네트워크 소유자가 자신의 네트워크를 회로에 연결하는 데 사용할 수 있는 권한 부여 키를 생성합니다(가상 네트워크당 하나의 권한 부여). 권한 부여 키 및 권한 부여에 대한 기타 정보는 **Get-AzExpressRouteCircuitAuthorization을** 실행하여 수시로 볼 수 있습니다.

## 예제

### 예제 1: 모든 ExpressRoute 권한 부여를 얻습니다.
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

이러한 명령은 ExpressRoute 회로와 연결된 모든 ExpressRoute 권한 부여에 대한 정보를 반환합니다. 첫 번째 명령은 **Get-AzExpressRouteCircuit** cmdlet을 사용하여 ContosoCircuit이라는 회로를 참조하는 개체를 만듭니다. 해당 개체 참조는 변수에 저장됩니다$Circuit. 그런 다음, 두 번째 명령은 해당 개체 참조 및 **Get-AzExpressRouteCircuitAuthorization** cmdlet을 사용하여 ContosoCircuit과 연결된 권한 부여에 대한 정보를 반환합니다.

### 예제 2: Where-Object cmdlet을 사용하여 모든 ExpressRoute 권한 부여를 얻습니다.
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

이러한 명령은 예제 1에 사용된 명령의 변형을 나타났습니다. 그러나 이 경우 사용할 수 있는 권한 부여(즉, 가상 네트워크에 할당되지 않은 권한 부여의 경우)에 대한 정보만 반환됩니다. 이를 위해 회로 권한 부여 정보는 명령 2에서 반환되어 **Where-Object** cmdlet으로 파이프됩니다.
**Where-Object는** *AuthorizationUseStatus* 속성이 사용 가능으로 설정된 권한 부여만 선택합니다. 사용할 수 없는 권한 부여만 나열하기 위해 Where 절에 대해 다음 구문을 사용하세요. `{$_.AuthorizationUseStatus -ne "Available"}`

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
ExpressRoute 회로 권한 부여를 지정합니다.

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
이 cmdlet에서 얻을 ExpressRoute 회로 권한 부여의 이름을 지정합니다.
-Name "ContosoCircuitAuthorization"

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## 출력

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization

## 참고 사항

## 관련 링크

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)
