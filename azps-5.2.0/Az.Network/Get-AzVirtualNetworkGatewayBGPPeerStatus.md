---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: 62fed5537cc22ee21679cbe1b8d126d9d30efb71
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370994"
---
# <span data-ttu-id="0c960-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="0c960-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="0c960-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c960-102">SYNOPSIS</span></span>
<span data-ttu-id="0c960-103">Azure 가상 네트워크 게이트웨이의 BGP 피어를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="0c960-103">Lists an Azure virtual network gateway's BGP peers</span></span>

## <span data-ttu-id="0c960-104">구문</span><span class="sxs-lookup"><span data-stu-id="0c960-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c960-105">설명</span><span class="sxs-lookup"><span data-stu-id="0c960-105">DESCRIPTION</span></span>
<span data-ttu-id="0c960-106">이 명령은 Azure 가상 네트워크 게이트웨이가 피어링하도록 구성된 BGP 피어를 열회합니다.</span><span class="sxs-lookup"><span data-stu-id="0c960-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="0c960-107">각 피어의 상태도 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c960-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="0c960-108">예제</span><span class="sxs-lookup"><span data-stu-id="0c960-108">EXAMPLES</span></span>

### <span data-ttu-id="0c960-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="0c960-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayBgpPeerStatus -ResourceGroupName resourceGroup -VirtualNetworkGatewayName gatewayName

Asn               : 65515
ConnectedDuration : 9.01:04:53.5768637
LocalAddress      : 10.1.0.254
MessagesReceived  : 14893
MessagesSent      : 14900
Neighbor          : 10.0.0.254
RoutesReceived    : 1
State             : Connected
```

<span data-ttu-id="0c960-110">리소스 그룹 resourceGroup에서 gatewayName이라는 Azure 가상 네트워크 게이트웨이에 대한 BGP 피어를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="0c960-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>
<span data-ttu-id="0c960-111">이 예제 출력은 IP가 10.0.0.254인 연결된 BGP 피어를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0c960-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="0c960-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c960-112">PARAMETERS</span></span>

### <span data-ttu-id="0c960-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c960-113">-AsJob</span></span>
<span data-ttu-id="0c960-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0c960-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c960-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c960-115">-DefaultProfile</span></span>
<span data-ttu-id="0c960-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c960-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c960-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="0c960-117">-Peer</span></span>
<span data-ttu-id="0c960-118">다음에 대한 상태를 검색할 피어의 IP</span><span class="sxs-lookup"><span data-stu-id="0c960-118">IP of the peer to retrieve status for</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c960-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c960-119">-ResourceGroupName</span></span>
<span data-ttu-id="0c960-120">가상 네트워크 게이트웨이 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="0c960-120">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="0c960-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="0c960-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="0c960-122">가상 네트워크 게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="0c960-122">Virtual network gateway name</span></span>

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

### <span data-ttu-id="0c960-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c960-123">CommonParameters</span></span>
<span data-ttu-id="0c960-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0c960-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c960-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0c960-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c960-126">입력</span><span class="sxs-lookup"><span data-stu-id="0c960-126">INPUTS</span></span>

### <span data-ttu-id="0c960-127">System.String</span><span class="sxs-lookup"><span data-stu-id="0c960-127">System.String</span></span>

## <span data-ttu-id="0c960-128">출력</span><span class="sxs-lookup"><span data-stu-id="0c960-128">OUTPUTS</span></span>

### <span data-ttu-id="0c960-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="0c960-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span></span>

## <span data-ttu-id="0c960-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0c960-130">NOTES</span></span>

## <span data-ttu-id="0c960-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c960-131">RELATED LINKS</span></span>
