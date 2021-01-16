---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 34f92bfa7566679c4cee9f7a4281ac15c55676b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326290"
---
# Get-AzApplicationGatewayHttpListenerCustomError

## SYNOPSIS
애플리케이션 게이트웨이의 http 수신기에서 사용자 지정 오류를 얻습니다.

## 구문

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Get-AzApplicationGatewayCustomError** cmdlet은 애플리케이션 게이트웨이의 http 수신기에서 사용자 지정 오류를 얻습니다.

## 예제

### 예제 1: http 수신기에서 사용자 지정 오류 발생
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

이 명령은 http 수신기 $listener 01에서 http 상태 코드 502의 사용자 지정 오류를 $listener.

### 예제 2: http 수신기에서 모든 사용자 지정 오류 목록을 얻습니다.
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

이 명령은 http listener $listener 01에서 모든 사용자 지정 오류 목록을 $listener.

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

### -HttpListener
Application Gateway Http 수신기

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StatusCode
애플리케이션 게이트웨이 고객 오류의 상태 코드입니다.

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

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener

## 출력

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError

## 참고 사항

## 관련 링크

[Add-AzApplicationGatewayHttpListenerCustomError](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[Remove-AzApplicationGatewayHttpListenerCustomError](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[Set-AzApplicationGatewayHttpListenerCustomError](./Set-AzApplicationGatewayHttpListenerCustomError.md)
