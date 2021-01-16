---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: a6a3b973a893e3588b5df77700318a725bde11b9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331274"
---
# Get-AzExpressRouteCrossConnection

## SYNOPSIS
Azure에서 Azure ExpressRoute 교차 연결을 얻습니다.

## 구문

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzExpressRouteCrossConnection** cmdlet은 구독에서 ExpressRoute 교차 연결 개체를 검색하는 데 사용됩니다.
AzureRmExpressRouteCrossConnection

## 예제

### 예제 1: ExpressRoute 교차 연결 얻기
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### 예제 2: 필터를 사용하여 ExpressRoute 교차 연결 나열
```
Get-AzExpressRouteCrossConnection -Name test*
```

이 cmdlet은 "test"로 시작하는 모든 ExpressRoute 교차 연결을 나열합니다.

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
ExpressRoute 교차 연결의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -ResourceGroupName
ExpressRoute 교차 연결을 포함하는 리소스 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### 없음
이 cmdlet은 입력을 허용하지 않습니다.

## 출력

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection

## 참고 사항

## 관련 링크

[Set-AzExpressRouteCrossConnection](Set-AzExpressRouteCrossConnection.md)