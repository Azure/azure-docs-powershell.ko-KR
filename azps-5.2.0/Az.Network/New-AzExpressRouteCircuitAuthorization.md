---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 28b45f5368fb7a63450276c054654313d7e1c517
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354902"
---
# New-AzExpressRouteCircuitAuthorization

## SYNOPSIS
ExpressRoute 회로 권한 부여를 만듭니다.

## 구문

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**New-AzExpressRouteCircuitAuthorization** cmdlet은 ExpressRoute 회로에 추가할 수 있는 회로 권한 부여를 만듭니다. ExpressRoute 회로는 공용 인터넷 대신 연결 공급자를 사용하여 Microsoft 클라우드에 연결합니다. ExpressRoute 회로의 소유자는 각 회로에 대해 10개까지 권한 부여를 만들 수 있습니다. 이러한 권한 부여는 가상 네트워크 소유자가 네트워크를 회로에 연결하는 데 사용할 수 있는 권한 부여 키를 생성합니다. 가상 네트워크당 하나의 권한 부여만 가능합니다.
ExpressRoute 회로를 만든 후 **Add-AzExpressRouteCircuitAuthorization을** 사용하여 해당 회로에 권한 부여를 추가할 수 있습니다.
또는 **New-AzExpressRouteCircuitAuthorization을** 사용하여 회로를 만드는 동시에 새 회로에 추가할 수 있는 권한 부여를 만들 수 있습니다.

## 예제

### 예제 1: 새 회로 권한 부여 만들기
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

이 명령은 ContosoCircuitAuthorization이라는 새 회로 권한 부여를 만든 다음, 해당 개체를 $Authorization. 개체를 변수에 저장하는 것이 중요합니다. **New-AzExpressRouteCircuitAuthorization이** 회로 권한 부여를 만들 수 있는 경우 회로 경로에 해당 권한 부여를 추가할 수 없습니다. 대신 새 ExpressRoute 회로를 $Authorization New-AzExpressRouteCircuit 변수가 사용됩니다.
자세한 내용은 New-AzExpressRouteCircuit cmdlet에 대한 설명서를 참조하세요.

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

### -Name
새 ExpressRoute 회로 권한 부여에 대한 고유한 이름을 지정합니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization

## 참고 사항

## 관련 링크

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

