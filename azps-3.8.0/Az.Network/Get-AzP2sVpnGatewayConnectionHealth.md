---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
ms.openlocfilehash: 4b9778275f58025c82922133cb5d6f6142df4fc8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033826"
---
# Get-AzP2sVpnGatewayConnectionHealth

## SYNOPSIS
P2SVpnGateway에서 사이트 연결 상태 정보에 대 한 현재 aggregared 지점을 가져옵니다.

## 구문과

### ByP2SVpnGatewayName (기본값)
```
Get-AzP2sVpnGatewayConnectionHealth [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByP2SVpnGatewayObject
```
Get-AzP2sVpnGatewayConnectionHealth -InputObject <PSP2SVpnGateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByP2SVpnGatewayResourceId
```
Get-AzP2sVpnGatewayConnectionHealth -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzP2sVpnGatewayConnectionHealth** cmdlet을 사용 하 여 P2SVpnGateway에서 사이트 연결에 대 한 현재 집계 된 상태를 가져올 수 있습니다. 집계 상태는 P2SVpnGateway에 연결 된 사이트 클라이언트의 수, P2SVpnGateway를 통해 전송 되는 총 수신 및 송신 바이트 및 연결 된 위치를 사이트 클라이언트에 할당할 ip 주소를 표시 합니다.

## 예제의

### 예제 1
```powershell
PS C:\> Get-AzP2sVpnGatewayConnectionHealth -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : { 
                  "VpnClientConnectionsCount": 2,
                      "AllocatedIpAddresses": { "192.168.2.1", "192.168.2.2" },
                      "TotalIngressBytesTransferred": 100,
                      "TotalEgressBytesTransferred": 200
                 }
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

**AzP2sVpnGatewayConnectionHealth** cmdlet을 사용 하 여 P2SVpnGateway에서 사이트 연결에 대 한 현재 집계 된 상태를 가져올 수 있습니다. 위의 명령 출력 상태는 P2SVpnGateway에 연결 된 사이트 클라이언트에 대 한 지점의 수가 2 인 것으로 표시 됩니다. P2SVpnGateway를 통해 전송 된 총 수신 및 송신 바이트는 각각 100 및 200입니다. 연결 된 지점의 사이트 클라이언트에 대해 할당 된 ip 주소는 "192.168.2.1", "192.168.2.2"입니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -InputObject
수정할 p2s vpn 게이트웨이 개체

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -이름
자원 이름입니다.

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
수정할 P2SVpnGateway의 Azure resource ID입니다.

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열
PSP2SVpnGateway에 대 한.

## 출력

### PSP2SVpnGateway에 대 한.

## 상속자

## 관련 링크
