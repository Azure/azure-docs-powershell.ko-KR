---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
ms.openlocfilehash: 4b9778275f58025c82922133cb5d6f6142df4fc8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193780"
---
# <span data-ttu-id="365b4-101">Get-AzP2sVpnGatewayConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="365b4-101">Get-AzP2sVpnGatewayConnectionHealth</span></span>

## <span data-ttu-id="365b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="365b4-102">SYNOPSIS</span></span>
<span data-ttu-id="365b4-103">P2SVpnGateway에서 현재 집계 지점과 사이트 연결 상태 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="365b4-103">Gets the current aggregared point to site connections health information from P2SVpnGateway.</span></span>

## <span data-ttu-id="365b4-104">구문</span><span class="sxs-lookup"><span data-stu-id="365b4-104">SYNTAX</span></span>

### <span data-ttu-id="365b4-105">ByP2SVpnGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="365b4-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="365b4-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="365b4-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -InputObject <PSP2SVpnGateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="365b4-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="365b4-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="365b4-108">설명</span><span class="sxs-lookup"><span data-stu-id="365b4-108">DESCRIPTION</span></span>
<span data-ttu-id="365b4-109">**Get-AzP2sVpnGatewayConnectionHealth** cmdlet을 사용하면 P2SVpnGateway에서 지점 및 사이트 간 연결의 현재 집계된 상태 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="365b4-109">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="365b4-110">집계된 상태는 P2SVpnGateway에 연결된 지점 및 사이트 클라이언트 수, P2SVpnGateway를 통해 전송된 총 송수신 및 송수신 bytes 및 연결된 지점 및 사이트 클라이언트에 할당된 IP 주소를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="365b4-110">Aggregated health shows number of point to site clients connected to P2SVpnGateway, total ingress and egress bytes transferred through P2SVpnGateway and allocated ip addresses for connected point to site clients.</span></span>

## <span data-ttu-id="365b4-111">예제</span><span class="sxs-lookup"><span data-stu-id="365b4-111">EXAMPLES</span></span>

### <span data-ttu-id="365b4-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="365b4-112">Example 1</span></span>
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

<span data-ttu-id="365b4-113">**Get-AzP2sVpnGatewayConnectionHealth** cmdlet을 사용하면 P2SVpnGateway에서 지점 및 사이트 간 연결의 현재 집계된 상태 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="365b4-113">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="365b4-114">위의 명령 let 출력 상태는 P2SVpnGateway에 연결된 지점 및 사이트 클라이언트 수가 2인 경우를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="365b4-114">Above command let output health shows that number of point to site clients connected to P2SVpnGateway are 2.</span></span> <span data-ttu-id="365b4-115">P2SVpnGateway를 통해 전송된 총 송수신 bytes는 각각 100 및 200입니다.</span><span class="sxs-lookup"><span data-stu-id="365b4-115">Total ingress and egress bytes transferred through P2SVpnGateway are 100 and 200 respectively.</span></span> <span data-ttu-id="365b4-116">연결된 지점 및 사이트 클라이언트에 할당된 IP 주소는 "192.168.2.1", "192.168.2.2"입니다.</span><span class="sxs-lookup"><span data-stu-id="365b4-116">Allocated ip addresses for connected point to site clients are "192.168.2.1", "192.168.2.2".</span></span>

## <span data-ttu-id="365b4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="365b4-117">PARAMETERS</span></span>

### <span data-ttu-id="365b4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="365b4-118">-DefaultProfile</span></span>
<span data-ttu-id="365b4-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="365b4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="365b4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="365b4-120">-InputObject</span></span>
<span data-ttu-id="365b4-121">수정할 p2s vpn Gateway 개체</span><span class="sxs-lookup"><span data-stu-id="365b4-121">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="365b4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="365b4-122">-Name</span></span>
<span data-ttu-id="365b4-123">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="365b4-123">The resource name.</span></span>

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

### <span data-ttu-id="365b4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="365b4-124">-ResourceGroupName</span></span>
<span data-ttu-id="365b4-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="365b4-125">The resource group name.</span></span>

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

### <span data-ttu-id="365b4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="365b4-126">-ResourceId</span></span>
<span data-ttu-id="365b4-127">수정할 P2SVpnGateway의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="365b4-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="365b4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="365b4-128">CommonParameters</span></span>
<span data-ttu-id="365b4-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="365b4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="365b4-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="365b4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="365b4-131">입력</span><span class="sxs-lookup"><span data-stu-id="365b4-131">INPUTS</span></span>

### <span data-ttu-id="365b4-132">System.String</span><span class="sxs-lookup"><span data-stu-id="365b4-132">System.String</span></span>
<span data-ttu-id="365b4-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="365b4-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="365b4-134">출력</span><span class="sxs-lookup"><span data-stu-id="365b4-134">OUTPUTS</span></span>

### <span data-ttu-id="365b4-135">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="365b4-135">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="365b4-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="365b4-136">NOTES</span></span>

## <span data-ttu-id="365b4-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="365b4-137">RELATED LINKS</span></span>
