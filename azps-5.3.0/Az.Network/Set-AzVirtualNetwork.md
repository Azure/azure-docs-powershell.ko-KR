---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 822b982b2c1714e2c0331cc9b64fe2c1753044f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491754"
---
# Set-AzVirtualNetwork

## SYNOPSIS
가상 네트워크를 업데이트합니다.

## 구문

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Set-AzVirtualNetwork** cmdlet은 가상 네트워크를 업데이트합니다.

## 예제

### 1: 가상 네트워크를 만들고 해당 서브넷 중 하나를 제거합니다.
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

이 예제에서는 frontendSubnet 및 backendSubnet이라는 두 개의 서브넷이 있는 TestResourceGroup이라는 가상 네트워크를 만듭니다. 그런 다음 가상 네트워크의 메모리 내 표현에서 backendSubnet 서브넷을 제거합니다. 그런 Set-AzVirtualNetwork cmdlet은 서비스 쪽에서 수정된 가상 네트워크 상태를 작성하는 데 사용됩니다. Set-AzVirtualNetwork cmdlet이 실행되면 backendSubnet이 제거됩니다.

## PARAMETERS

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

### -VirtualNetwork
가상 네트워크를 설정해야 하는 상태를 나타내는 가상 네트워크 개체를 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork

## 출력

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork

## 참고 사항

## 관련 링크

[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)

[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)

[New-AzVirtualNetwork](./New-AzVirtualNetwork.md)

[Remove-AzVirtualNetwork](./Remove-AzVirtualNetwork.md)


