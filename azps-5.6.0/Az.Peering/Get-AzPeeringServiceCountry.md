---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringservicecountry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceCountry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceCountry.md
ms.openlocfilehash: 4f13c0be9681fb2eda6fa509e321c2fa161049ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989487"
---
# Get-AzPeeringServiceCountry

## SYNOPSIS
피어링 서비스에 사용할 수 있는 국가를 나열합니다.

## 구문

```
Get-AzPeeringServiceCountry [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
피어링 서비스에 사용할 수 있는 국가를 나열합니다.

## 예제

### 예제 1
```powershell
PS C:\> Get-AzPeeringServiceCountry
```

피어링 서비스에 사용할 수 있는 국가 목록입니다.

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

### Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation

## 참고 사항

## 관련 링크
