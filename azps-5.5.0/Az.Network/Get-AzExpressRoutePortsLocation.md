---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 918ef18717cb09bad28ee10b91f635181dd5b3cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189785"
---
# Get-AzExpressRoutePortsLocation

## SYNOPSIS
ExpressRoutePort 리소스를 사용할 수 있는 위치를 얻습니다.

## 구문

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Get-AzExpressRoutePortsLocation** cmdlet은 ExpressRoutePort 리소스를 사용할 수 있는 위치를 검색하는 데 사용됩니다. 특정 위치를 입력으로 지정하면 cmdlet에 해당 위치의 세부 정보(예: 해당 위치의 사용 가능한 대역폭 목록)가 표시됩니다.

## 예제

### 예제 1
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

ExpressRoutePort 리소스를 사용할 수 있는 위치를 나열합니다.

### 예제 2
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

위치 및 위치에서 사용할 수 있는 ExpressRoutePort 대역폭을 $loc.

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

### -LocationName
위치의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation

## 참고 사항

## 관련 링크
