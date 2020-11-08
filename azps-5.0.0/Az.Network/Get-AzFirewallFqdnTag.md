---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 84d42e18e1946b96a2102a51f71af7e879867d57
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218843"
---
# Get-AzFirewallFqdnTag

## SYNOPSIS
사용할 수 있는 Azure 방화벽 Fqdn 태그를 가져옵니다.

## 구문과

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzFirewallFqdnTag** Cmdlet은 Azure 방화벽 응용 프로그램 규칙에 사용할 수 있는 FQDN 태그 목록을 가져옵니다.

## 예제의

### 1: 사용 가능한 모든 FQDN 태그 검색
```
Get-AzFirewallFqdnTag
```

이 예제에서는 사용 가능한 모든 FQDN 태그를 검색 합니다.

### 2: 응용 프로그램 규칙에서 사용할 수 있는 첫 번째 FQDN 태그 사용
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

이 예제에서는 사용 가능한 첫 번째 FQDN 태그를 사용 하 여 방화벽 응용 프로그램 규칙을 만듭니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### 않아야

## 출력

### PSAzureFirewallFqdnTag에 대 한.

### System.webserver. t e 1 [[Microsoft PSAzureFirewallFqdnTag, Microsoft azure. e 1. *. PowerShell, 버전 = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]

## 상속자

## 관련 링크

[새로운 AzFirewallApplicationRule](./New-AzFirewallApplicationRule.md)

[새로운 AzFirewall](./New-AzFirewall.md)
