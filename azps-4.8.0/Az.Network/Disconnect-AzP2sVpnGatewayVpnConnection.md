---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azp2svpngatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2sVpnGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2sVpnGatewayVpnConnection.md
ms.openlocfilehash: ee14842a636ff451e100a75db427934f9f0a1043
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056235"
---
# <span data-ttu-id="53c9a-101">Disconnect-AzP2sVpnGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="53c9a-101">Disconnect-AzP2sVpnGatewayVpnConnection</span></span>

## <span data-ttu-id="53c9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53c9a-102">SYNOPSIS</span></span>
<span data-ttu-id="53c9a-103">지정 된 p2s vpn 게이트웨이를 사용 하 여 연결 된 특정 vpn 클라이언트 연결 연결 끊기</span><span class="sxs-lookup"><span data-stu-id="53c9a-103">Disconnect given connected vpn client connections with a given p2s vpn gateway</span></span>

## <span data-ttu-id="53c9a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="53c9a-104">SYNTAX</span></span>

### <span data-ttu-id="53c9a-105">ByP2SVpnGatewayName (기본값)</span><span class="sxs-lookup"><span data-stu-id="53c9a-105">ByP2SVpnGatewayName (Default)</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -Name <String> -ResourceGroupName <String>
 -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="53c9a-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="53c9a-106">ByP2SVpnGatewayObject</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="53c9a-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="53c9a-107">ByP2SVpnGatewayResourceId</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="53c9a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="53c9a-108">DESCRIPTION</span></span>
<span data-ttu-id="53c9a-109">**AzP2sVpnGatewayVpnConnection** cmdlet을 사용 하면 주어진 현재 지점의 P2SVpnGateway에서 사이트 연결을 끊을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53c9a-109">The **Disconnect-AzP2sVpnGatewayVpnConnection** cmdlet enables you to disconnect given current point to site connection from P2SVpnGateway.</span></span>

## <span data-ttu-id="53c9a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="53c9a-110">EXAMPLES</span></span>

### <span data-ttu-id="53c9a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="53c9a-111">Example 1</span></span>
```powershell
PS C:\> Disconnect-AzP2sVpnGatewayVpnConnection -ResourceName 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
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

## <span data-ttu-id="53c9a-112">변수</span><span class="sxs-lookup"><span data-stu-id="53c9a-112">PARAMETERS</span></span>

### <span data-ttu-id="53c9a-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53c9a-113">-InputObject</span></span>
<span data-ttu-id="53c9a-114">수정할 p2s vpn 게이트웨이 개체</span><span class="sxs-lookup"><span data-stu-id="53c9a-114">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53c9a-115">-이름</span><span class="sxs-lookup"><span data-stu-id="53c9a-115">-Name</span></span>
<span data-ttu-id="53c9a-116">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53c9a-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53c9a-117">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="53c9a-117">-VpnConnectionId</span></span>
<span data-ttu-id="53c9a-118">Vpn 연결 Ida</span><span class="sxs-lookup"><span data-stu-id="53c9a-118">Vpn Connection Ida</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53c9a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53c9a-119">-ResourceGroupName</span></span>
<span data-ttu-id="53c9a-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53c9a-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53c9a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53c9a-121">-ResourceId</span></span>
<span data-ttu-id="53c9a-122">P2s 가상 네트워크 게이트웨이 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="53c9a-122">P2s Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53c9a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53c9a-123">CommonParameters</span></span>
<span data-ttu-id="53c9a-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="53c9a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53c9a-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53c9a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53c9a-126">입력</span><span class="sxs-lookup"><span data-stu-id="53c9a-126">INPUTS</span></span>

### <span data-ttu-id="53c9a-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="53c9a-127">System.String</span></span>

## <span data-ttu-id="53c9a-128">출력</span><span class="sxs-lookup"><span data-stu-id="53c9a-128">OUTPUTS</span></span>

### <span data-ttu-id="53c9a-129">PSP2SVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="53c9a-129">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="53c9a-130">상속자</span><span class="sxs-lookup"><span data-stu-id="53c9a-130">NOTES</span></span>

## <span data-ttu-id="53c9a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53c9a-131">RELATED LINKS</span></span>
