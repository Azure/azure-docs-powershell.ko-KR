---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
ms.openlocfilehash: 94375ba7d54095af131d7a61c7b06d50e2ba9521
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184364"
---
# New-AzPrivateLinkServiceIpConfig

## SYNOPSIS
개인 링크 서비스 IP 구성을 생성합니다.

## 구문

```
New-AzPrivateLinkServiceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-PublicIpAddress <PSPublicIpAddress>]
 [-Subnet <PSSubnet>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**New-AzPrivateLinkServiceIpConfig** cmdlet은 개인 링크 서비스 IP 구성을 만듭니다. 이 구성은 개인 엔드포인트에서 들어오는 트래픽을 원본 NAT에 수신하는 데 사용됩니다. 

## 예제

### 예제 1
```powershell
New-AzPrivateLinkServiceIpConfig -Name $IpConfigurationName -PrivateIpAddress "10.0.0.5" -Primary
```

이 예제에서는 메모리에 개인 링크 서비스 IP 구성을 생성합니다.

### 예제 2

개인 링크 서비스 IP 구성을 생성합니다. (자동Generated)

<!-- Aladdin Generated Example -->
```powershell
New-AzPrivateLinkServiceIpConfig -Name 'IP-Config' -PrivateIpAddress '10.0.0.5' -Subnet <PSSubnet>
```

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
IpConfiguration의 이름

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIpAddress
고정 할당이 지정된 경우 ipConfiguration의 개인 IP 주소입니다.

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

### -PrivateIpAddressVersion
IP 구성의 IP 버전

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Primary
현재 IP 구성이 기본 구성인지 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnet
서브넷

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
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

### 없음

## 출력

### Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration

## 참고 사항

## 관련 링크

[New-AzPrivateLinkService](./New-AzPrivateLinkService.md)