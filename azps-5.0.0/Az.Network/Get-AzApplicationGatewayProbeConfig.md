---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: ec20d7caafe110f03e5a0ce3130247ec877d6af9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226708"
---
# Get-AzApplicationGatewayProbeConfig

## SYNOPSIS
응용 프로그램 게이트웨이에서 기존 상태 프로브 구성을 가져옵니다.

## 구문과

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
Get-AzApplicationGatewayProbeConfig cmdlet은 응용 프로그램 게이트웨이에서 기존 상태 프로브 구성을 가져옵니다.

## 예제의

### 예제 1: 응용 프로그램 게이트웨이에서 기존 프로브 가져오기
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

이 명령은 Gateway 라는 응용 프로그램 게이트웨이에서 Probe02 이라는 상태 프로브를 가져옵니다.

## 변수

### -ApplicationGateway
이 cmdlet이 프로브 구성을 가져오는 응용 프로그램 게이트웨이를 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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
프로브의 이름을 지정 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### Microsoft. * PSApplicationGateway

## 출력

### Microsoft. *. m i m a. 모델. m i m a 검색

## 상속자

## 관련 링크

[기존 application gateway에 프로브 추가](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[추가-AzApplicationGatewayProbeConfig](./Add-AzApplicationGatewayProbeConfig.md)

[새로운 AzApplicationGatewayProbeConfig](./New-AzApplicationGatewayProbeConfig.md)

[제거-AzApplicationGatewayProbeConfig](./Remove-AzApplicationGatewayProbeConfig.md)

[Set-AzApplicationGatewayProbeConfig](./Set-AzApplicationGatewayProbeConfig.md)

