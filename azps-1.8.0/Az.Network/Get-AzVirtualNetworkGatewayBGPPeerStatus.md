---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: 416bc8910e651ca86ef064fda7bd934d67ed8056
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700482"
---
# <span data-ttu-id="95729-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="95729-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="95729-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95729-102">SYNOPSIS</span></span>
<span data-ttu-id="95729-103">Azure 가상 네트워크 게이트웨이의 BGP 피어를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="95729-103">Lists an Azure virtual network gateway's BGP peers</span></span>

## <span data-ttu-id="95729-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95729-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95729-105">설명은</span><span class="sxs-lookup"><span data-stu-id="95729-105">DESCRIPTION</span></span>
<span data-ttu-id="95729-106">이 명령은 Azure 가상 네트워크 게이트웨이가 피어로 구성 된 BGP 피어를 열거 합니다.</span><span class="sxs-lookup"><span data-stu-id="95729-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="95729-107">각 피어의 상태도 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95729-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="95729-108">예제의</span><span class="sxs-lookup"><span data-stu-id="95729-108">EXAMPLES</span></span>

### <span data-ttu-id="95729-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="95729-109">Example 1</span></span>
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

<span data-ttu-id="95729-110">리소스 그룹 리소스 \에 있는 게이트웨이 이름 이라는 Azure 가상 네트워크 게이트웨이의 BGP 피어를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="95729-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>
<span data-ttu-id="95729-111">이 예제 출력에서는 10.0.0.254의 IP를 사용 하 여 연결 된 BGP 피어 하나를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="95729-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="95729-112">변수</span><span class="sxs-lookup"><span data-stu-id="95729-112">PARAMETERS</span></span>

### <span data-ttu-id="95729-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95729-113">-AsJob</span></span>
<span data-ttu-id="95729-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="95729-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95729-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95729-115">-DefaultProfile</span></span>
<span data-ttu-id="95729-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95729-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95729-117">-투-피어</span><span class="sxs-lookup"><span data-stu-id="95729-117">-Peer</span></span>
<span data-ttu-id="95729-118">상태를 검색할 피어의 IP</span><span class="sxs-lookup"><span data-stu-id="95729-118">IP of the peer to retrieve status for</span></span>

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

### <span data-ttu-id="95729-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95729-119">-ResourceGroupName</span></span>
<span data-ttu-id="95729-120">가상 네트워크 게이트웨이 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="95729-120">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="95729-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="95729-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="95729-122">가상 네트워크 게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="95729-122">Virtual network gateway name</span></span>

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

### <span data-ttu-id="95729-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95729-123">CommonParameters</span></span>
<span data-ttu-id="95729-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95729-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95729-125">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="95729-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95729-126">입력</span><span class="sxs-lookup"><span data-stu-id="95729-126">INPUTS</span></span>

### <span data-ttu-id="95729-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="95729-127">System.String</span></span>

## <span data-ttu-id="95729-128">출력</span><span class="sxs-lookup"><span data-stu-id="95729-128">OUTPUTS</span></span>

### <span data-ttu-id="95729-129">PSBGPPeerStatus에 대 한.</span><span class="sxs-lookup"><span data-stu-id="95729-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span></span>

## <span data-ttu-id="95729-130">상속자</span><span class="sxs-lookup"><span data-stu-id="95729-130">NOTES</span></span>

## <span data-ttu-id="95729-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95729-131">RELATED LINKS</span></span>
