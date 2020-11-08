---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226361"
---
# Remove-AzExpressRouteCircuitAuthorization

## SYNOPSIS
기존 Express 경로 구성 권한 부여를 제거 합니다.

## 구문과

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzExpressRouteCircuitAuthorization** Cmdlet은 express 경로 회로에 할당 된 인증을 제거 합니다. Express 경로 회로는 공용 인터넷 대신 연결 공급자를 사용 하 여 온-프레미스 네트워크를 Azure에 연결 합니다. Express 경로 회로의 소유자는 각 회로에 대해 최대 10 개의 권한을 만들 수 있습니다. 이러한 권한 부여는 가상 네트워크 소유자가 네트워크를 회로에 연결 하는 데 사용할 수 있는 인증 키를 생성 합니다. 가상 네트워크 당 하나의 권한 부여만 있을 수 있습니다. 그러나 언제 든 지 회로 소유자는 **제거-AzExpressRouteCircuitAuthorization** 를 사용 하 여 가상 네트워크에 할당 된 권한을 제거할 수 있습니다. 이 경우 해당 가상 네트워크는 더 이상 대상 경로를 사용 하 여 Azure에 연결할 수 없습니다.

## 예제의

### 예제 1: Express 회로에서 회로 승인 제거
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

이 예제에서는 Express 경로 회로에서 회로 인증을 제거 합니다. 첫 번째 명령은 **AzExpressRouteCircuit** cmdlet을 사용 하 여 ContosoCircuit 이라는 express 경로에 대 한 개체 참조를 만들고 결과를 $Circuit 이라는 변수에 저장 합니다.
두 번째 명령은 회로 권한 부여 ContosoCircuitAuthorization 제거를 표시 합니다.
세 번째 명령은 Set-AzExpressRouteCircuit cmdlet을 사용 하 여 $Circuit 변수에 저장 된 Express 대상 회로가 제거 되었는지 확인 합니다.

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
이 cmdlet이 제거 하는 ExpressRouteCircuit 개체를 지정 합니다.

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
이 cmdlet이 제거 하는 회로 권한 부여의 이름을 지정 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSExpressRouteCircuit에 대 한.

## 출력

### PSExpressRouteCircuit에 대 한.

## 상속자

## 관련 링크

[추가-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[새로운 AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
