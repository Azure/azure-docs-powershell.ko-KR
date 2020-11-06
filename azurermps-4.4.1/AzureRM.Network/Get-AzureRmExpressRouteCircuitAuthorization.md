---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: a99b2ce5364e256f19069e1142b49abaf7f5e938
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537844"
---
# Get-AzureRmExpressRouteCircuitAuthorization

## SYNOPSIS
Express 경로 권한 부여에 대 한 정보를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmExpressRouteCircuitAuthorization** Cmdlet은 express 경로 회로에 할당 된 권한 부여에 대 한 정보를 가져옵니다. Express 경로 회로는 공용 인터넷 대신 연결 공급자를 사용 하 여 온-프레미스 네트워크를 Microsoft 클라우드에 연결 합니다. Express 경로 회로의 소유자는 각 회로에 대해 최대 10 개의 권한을 만들 수 있습니다. 이러한 권한 부여는 가상 네트워크 소유자가 네트워크를 회로에 연결 하는 데 사용할 수 있는 인증 키를 생성 합니다 (가상 네트워크 당 하나의 권한 부여). 인증 키 및 권한 부여에 대 한 기타 정보는 **AzureRmExpressRouteCircuitAuthorization** 를 실행 하 여 언제 든 지 볼 수 있습니다.

## 예제의

### 예제 1: 모든 Express 위치 권한 부여 가져오기
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit
```

이러한 명령은 Express 경로 회로와 연결 된 모든 Express 권한 부여에 대 한 정보를 반환 합니다. 첫 번째 명령은 **AzureRmExpressRouteCircuit** cmdlet을 사용 하 여 개체 참조 (ContosoCircuit 라는 회로)를 만듭니다. 해당 개체 참조는 변수 $Circuit에 저장 됩니다. 그런 다음 두 번째 명령은 해당 개체 참조 및 **AzureRmExpressRouteCircuitAuthorization** cmdlet을 사용 하 여 ContosoCircuit와 연결 된 권한 부여에 대 한 정보를 반환 합니다.

### 예제 2: Where-Object cmdlet을 사용 하 여 모든 Express 경로 권한 부여 가져오기
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

이러한 명령은 예제 1에 사용 된 명령의 변형을 나타냅니다. 그러나이 경우에는 사용할 수 있는 권한 부여 (즉, 가상 네트워크에 할당 되지 않은 권한 부여)에 대해서만 정보가 반환 됩니다. 이렇게 하려면 회로 인증 정보가 명령 2에 반환 되 고, **Where-Object** cmdlet에 대 한 것으로 처리 됩니다.
**여기서-Object** 는 *AuthorizationUseStatus* 속성이 사용 가능으로 설정 된 권한 부여만 선택 합니다. 사용할 수 없는 권한 부여만 나열 하려면 Where 절에 다음 구문을 사용 합니다.

`{$_.AuthorizationUseStatus -ne "Available"}`

## 변수

### -ExpressRouteCircuit
Express 경로 회로 인증을 지정 합니다.

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
이 cmdlet이 가져오는 Express 경로에 대 한 회로 권한 부여의 이름을 지정 합니다.

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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSExpressRouteCircuit
**Get-AzureRmExpressRouteCircuitAuthorization** 는 **PSExpressRouteCircuit** 개체의 파이프라인 인스턴스를 허용 합니다.

## 출력

### PSExpressRouteCircuitAuthorization
**Get-AzureRmExpressRouteCircuitAuthorization** **PSExpressRouteCircuitAuthorization** 개체의 인스턴스를 반환 합니다.

## 상속자

## 관련 링크

[추가-AzureRmExpressRouteCircuitAuthorization](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-AzureRmExpressRouteCircuit](./Get-AzureRmExpressRouteCircuit.md)

[새로운 AzureRmExpressRouteCircuitAuthorization](./New-AzureRmExpressRouteCircuitAuthorization.md)

[제거-AzureRmExpressRouteCircuitAuthorization](./Remove-AzureRmExpressRouteCircuitAuthorization.md)
