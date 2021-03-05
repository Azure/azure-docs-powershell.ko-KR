---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 33712b9813d6c23ed72097597d94a22bf7644992
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990948"
---
# Set-AzPublicIpAddress

## SYNOPSIS
공용 IP 주소를 업데이트합니다.

## 구문

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Set-AzPublicIpAddress** cmdlet은 공용 IP 주소를 업데이트합니다.

## 예제

### 1: 공용 IP 주소의 할당 방법 변경
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 첫 번째 명령은 리소스 그룹에서 이름과 함께 $publicIPName IP 주소 리소스를 $rgName.
두 번째 명령은 공용 IP 주소 개체의 할당 메서드를 "정적"으로 설정합니다.
Set-AzPublicIPAddress 업데이트된 개체로 공용 IP 주소 리소스를 업데이트하고 할당 메서드를 'Static'으로 수정합니다. 공용 IP 주소가 즉시 할당됩니다.

### 2: 공용 IP 주소의 DNS 도메인 레이블 추가
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

첫 번째 명령은 리소스 그룹에서 이름과 함께 $publicIPName IP 주소 리소스를 $rgName.
두 번째 명령은 DomainNameLabel 속성을 필요한 dns 연결로 설정합니다.
Set-AzPublicIPAddress 명령은 업데이트된 개체로 공용 IP 주소 리소스를 업데이트합니다. DomainNameLabel & Fqdn은 예상대로 수정됩니다.
    
### 3: 공용 IP 주소의 DNS 도메인 레이블 변경
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

첫 번째 명령은 리소스 그룹에서 이름과 함께 $publicIPName IP 주소 리소스를 $rgName.
두 번째 명령은 DomainNameLabel 속성을 필요한 dns 연결로 설정합니다.
Set-AzPublicIPAddress 명령은 업데이트된 개체로 공용 IP 주소 리소스를 업데이트합니다. DomainNameLabel & Fqdn은 예상대로 수정됩니다.

## 매개 변수

### -AsJob
백그라운드에서 cmdlet 실행

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

### -PublicIpAddress
공용 IP 주소를 설정해야 하는 상태를 나타내는 공용 IP 주소 개체를 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress

## 출력

### Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress

## 참고 사항

## 관련 링크

[Get-AzPublicIpAddress](./Get-AzPublicIpAddress.md)

[New-AzPublicIpAddress](./New-AzPublicIpAddress.md)

[Remove-AzPublicIpAddress](./Remove-AzPublicIpAddress.md)


