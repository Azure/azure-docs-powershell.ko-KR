---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservicecountry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceCountry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceCountry.md
ms.openlocfilehash: f1e324d03990b5a9ec82a315d9e84e0a1832de64
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384882"
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

### Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation

## 참고 사항

## 관련 링크
