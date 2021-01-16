---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: fc60a983e06e632912e43291f7b60980ff34a8cd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334922"
---
# New-AzFirewallHubPublicIpAddress

## SYNOPSIS
가상 허브의 방화벽에 연결된 공용 IP

## 구문

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
가상 허브의 방화벽에 연결된 공용 IP

## 예제

### 예제 1
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

이렇게 하면 가상 허브에 연결된 방화벽에 2개 공용 IP가 생성됩니다. 이렇게 하면 백end에 IP 주소가 생성됩니다. 새 방화벽에 대해 ipaddresses를 명시적으로 제공할 수 없습니다.

### 예제 2
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

이렇게 하면 방화벽에 이미 있는 $publicIp 1, $publicIp 2를 유지하여 방화벽에 1개 새 공용 IP가 생성됩니다.

## PARAMETERS

### -Addresses
허브에 연결된 방화벽의 공용 IP 주소

```yaml
Type: PSAzureFirewallPublicIpAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Count
공용 IP 주소 수

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: IAzureContextContainer
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

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses

## 참고 사항

## 관련 링크
