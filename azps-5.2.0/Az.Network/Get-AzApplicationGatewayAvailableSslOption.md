---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: f2175583aaaf3af04120e22e32db79d7b20f1e30
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354122"
---
# Get-AzApplicationGatewayAvailableSslOption

## SYNOPSIS
Application Gateway에 대한 ssl 정책에 사용 가능한 모든 ssl 옵션을 얻습니다.

## 구문

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzApplicationGatewayAvailableSslOption** cmdlet은 ssl 정책에 사용 가능한 모든 ssl 옵션을 제공합니다.

## 예제

### 예제 1
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

이 명령은 ssl 정책에 사용 가능한 모든 ssl 옵션을 반환합니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions

## 참고 사항

## 관련 링크
