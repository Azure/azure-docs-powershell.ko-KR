---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: 13a81733ac748d2593df967268021f10d60de50b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964288"
---
# <span data-ttu-id="763ab-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="763ab-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="763ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="763ab-102">SYNOPSIS</span></span>
<span data-ttu-id="763ab-103">Azure 가상 네트워크 게이트웨이에서 보급되는 경로를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="763ab-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

## <span data-ttu-id="763ab-104">구문</span><span class="sxs-lookup"><span data-stu-id="763ab-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="763ab-105">설명</span><span class="sxs-lookup"><span data-stu-id="763ab-105">DESCRIPTION</span></span>
<span data-ttu-id="763ab-106">BGP 피어의 IP를 지정하면 지정된 Azure 가상 네트워크 게이트웨이에 의해 해당 피어에 보급되는 경로를 열소합니다.</span><span class="sxs-lookup"><span data-stu-id="763ab-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="763ab-107">예제</span><span class="sxs-lookup"><span data-stu-id="763ab-107">EXAMPLES</span></span>

### <span data-ttu-id="763ab-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="763ab-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="763ab-109">리소스 그룹 리소스GroupName에서 gatewayName이라는 Azure 게이트웨이의 경우 IP 10.0.0.254를 사용하여 BGP 피어에 보급되는 경로 목록을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="763ab-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="763ab-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="763ab-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="763ab-111">리소스 그룹 리소스GroupName의 GatewayName이라는 Azure 게이트웨이의 경우 게이트웨이의 BGP 피어 목록에서 첫 번째 BGP 피어에 보급되는 경로를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="763ab-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="763ab-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="763ab-112">PARAMETERS</span></span>

### <span data-ttu-id="763ab-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="763ab-113">-AsJob</span></span>
<span data-ttu-id="763ab-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="763ab-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="763ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="763ab-115">-DefaultProfile</span></span>
<span data-ttu-id="763ab-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="763ab-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="763ab-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="763ab-117">-Peer</span></span>
<span data-ttu-id="763ab-118">BGP 피어의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="763ab-118">BGP peer's IP address.</span></span> <span data-ttu-id="763ab-119">이 IP는 게이트웨이가 배포된 Azure 가상 네트워크 내에서 액세스할 수 있는 주소 공간 내의 IP입니다.</span><span class="sxs-lookup"><span data-stu-id="763ab-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="763ab-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="763ab-120">-ResourceGroupName</span></span>
<span data-ttu-id="763ab-121">가상 네트워크 게이트웨이 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="763ab-121">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="763ab-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="763ab-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="763ab-123">가상 네트워크 게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="763ab-123">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="763ab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="763ab-124">CommonParameters</span></span>
<span data-ttu-id="763ab-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="763ab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="763ab-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="763ab-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="763ab-127">입력</span><span class="sxs-lookup"><span data-stu-id="763ab-127">INPUTS</span></span>

### <span data-ttu-id="763ab-128">System.String</span><span class="sxs-lookup"><span data-stu-id="763ab-128">System.String</span></span>

## <span data-ttu-id="763ab-129">출력</span><span class="sxs-lookup"><span data-stu-id="763ab-129">OUTPUTS</span></span>

### <span data-ttu-id="763ab-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="763ab-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="763ab-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="763ab-131">NOTES</span></span>
<span data-ttu-id="763ab-132">이 명령은 BGP가 설정된 연결을 사용하는 Azure 가상 네트워크 게이트웨이에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="763ab-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="763ab-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="763ab-133">RELATED LINKS</span></span>
