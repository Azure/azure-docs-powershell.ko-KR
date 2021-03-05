---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: b16206fdcaf775315947ca9fe71f487d1f9d8df1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011915"
---
# Add-AzExpressRouteCrossConnectionPeering

## SYNOPSIS
ExpressRoute 교차 연결에 피어링 구성을 추가합니다.

## 구문

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Add-AzExpressRouteCrossConnectionPeering** cmdlet은 ExpressRoute 교차 연결에 피어링 구성을 추가합니다. **Add-AzExpressRouteCrossConnectionPeering을** 실행한 후 구성을 활성화하려면 Set-AzExpressRouteCrossConnection cmdlet을 호출해야 합니다.

## 예제

### 예제 1: 기존 ExpressRoute 교차 연결에 피어 추가
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    CrossConnection = $cc
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCrossConnectionPeering @parameters
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

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

### -ExpressRouteCrossConnection
수정되는 ExpressRoute 교차 연결입니다. **Get-AzExpressRouteCrossConnection** cmdlet에서 반환되는 Azure 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.

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

### -MicrosoftConfigAdvertisedPublicPrefix
MicrosoftPeering의 PeeringType의 경우 BGP 세션을 통해 보급하려는 모든 사전 목록을 제공해야 합니다. 공용 IP 주소 도두사만 허용됩니다. 콤마로 구분된 목록을 보낼 수 있습니다. 이러한 사전은 라우팅 레지스트리 이름(RIR/IRR)에 등록해야 합니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MicrosoftConfigCustomerAsn
피어링 AS 번호에 등록되지 않은 광고 도두사인 경우 등록된 AS 번호를 지정할 수 있습니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MicrosoftConfigRoutingRegistryName
AS 번호 및 약어가 등록되는 라우팅 레지스트리 이름(RIR/IRR)입니다.

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

### -Name
추가할 피어링 관계의 이름입니다.

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

### -PeerAddressType
PeerAddressType

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PeerASN
ExpressRoute 교차 연결의 AS 수입니다. PeeringType이 AzurePublicPeering인 경우 공용 ASN이 되어야 합니다.

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PeeringType
이 매개 변수에 대해 허용되는 값은 `AzurePrivatePeering` , `AzurePublicPeering` , 및 `MicrosoftPeering`

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryPeerAddressPrefix
이 피어링 관계의 기본 라우팅 경로에 대한 IP 주소 범위입니다. /30 CIDR 서브넷이 되어야 합니다. 이 서브넷의 첫 번째 홀수 번호 주소는 라우터 인터페이스에 할당해야 합니다. Azure는 Azure 라우터 인터페이스에 대한 다음 조차 번호 매기기 주소를 구성합니다.

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

### -SecondaryPeerAddressPrefix
이 피어링 관계의 보조 라우팅 경로에 대한 IP 주소 범위입니다. /30 CIDR 서브넷이 되어야 합니다. 이 서브넷의 첫 번째 홀수 번호 주소는 라우터 인터페이스에 할당해야 합니다. Azure는 Azure 라우터 인터페이스에 대한 다음 조차 번호 매기기 주소를 구성합니다.

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

### -SharedKey
피어링 구성에 대한 사전 공유 키로 사용되는 선택적 MD5 해시입니다.

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

### -VlanId
이 피어링에 할당된 VLAN의 ID 번호입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다. cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### PSExpressRouteCrossConnection
매개 변수 'ExpressRouteCrossConnection'은 파이프라인에서 'PSExpressRouteCrossConnection' 형식의 값을 허용합니다.

## 출력

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection

## 참고 사항

## 관련 링크

[Get-AzExpressRouteCrossConnectionPeering](Get-AzExpressRouteCrossConnectionPeering.md)

[Remove-AzExpressRouteCrossConnectionPeering](Remove-AzExpressRouteCrossConnectionPeering.md)

[Get-AzExpressRouteCrossConnection](Get-AzExpressRouteCrossConnection.md)

[Set-AzExpressRouteCrossConnection](Set-AzExpressRouteCrossConnection.md)
