---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: 8d2022f79dff5263f07737d525169dad3566fcda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003643"
---
# Get-AzApplicationGatewayAvailableSslOption

## SYNOPSIS
Application Gateway에 대한 ssl 정책에 사용할 수 있는 모든 ssl 옵션을 제공합니다.

## 구문

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzApplicationGatewayAvailableSslOption** cmdlet은 ssl 정책에 사용할 수 있는 모든 ssl 옵션을 제공합니다.

## 예제

### 예제 1
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

이 명령은 ssl 정책에 사용할 수 있는 모든 ssl 옵션을 반환합니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions

## 참고 사항

## 관련 링크
