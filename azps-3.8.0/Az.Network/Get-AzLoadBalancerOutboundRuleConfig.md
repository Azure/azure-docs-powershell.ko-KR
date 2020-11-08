---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: b8683d461fe442ec0ad20098766d975b4cd6ae73
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043333"
---
# Get-AzLoadBalancerOutboundRuleConfig

## SYNOPSIS
부하 분산 장치에서 아웃 바운드 규칙 구성을 가져옵니다.

## 구문과

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzLoadBalancerOutboundRuleConfig** cmdlet은 아웃 바운드 규칙 구성 또는 부하 분산 장치에 대 한 아웃 바운드 규칙 구성 목록을 가져옵니다.

## 예제의

### 예제 1: 부하 분산 장치에서 아웃 바운드 규칙 구성 가져오기
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음이를 변수 $slb에 저장 합니다.
두 번째 명령은 해당 부하 분산 장치에 연결 된 MyRule 이라는 아웃 바운드 규칙 구성을 가져옵니다.

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

### -LoadBalancer
부하 분산 장치 리소스의 참조입니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -이름
아웃 바운드 규칙의 이름입니다.

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

### Microsoft. 네트워크. PSLoadBalancer

## 출력

### PSOutboundRule에 대 한.

## 상속자

## 관련 링크

[추가-AzLoadBalancerOutboundRuleConfig](./Add-AzLoadBalancerOutboundRuleConfig.md)

[새로운 AzLoadBalancerOutboundRuleConfig](./New-AzLoadBalancerOutboundRuleConfig.md)

[제거-AzLoadBalancerOutboundRuleConfig](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[Set-AzLoadBalancerOutboundRuleConfig](./Set-AzLoadBalancerOutboundRuleConfig.md)
