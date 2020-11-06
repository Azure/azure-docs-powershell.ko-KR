---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: 42960533c33cc2d5f8f4ee809cdd7a25c483c75d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531137"
---
# <span data-ttu-id="6d29e-101">Get-AzureRmVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="6d29e-101">Get-AzureRmVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="6d29e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d29e-102">SYNOPSIS</span></span>
<span data-ttu-id="6d29e-103">Azure 가상 네트워크 게이트웨이의 BGP 피어를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d29e-103">Lists an Azure virtual network gateway's BGP peers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d29e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6d29e-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d29e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6d29e-105">DESCRIPTION</span></span>
<span data-ttu-id="6d29e-106">이 명령은 Azure 가상 네트워크 게이트웨이가 피어로 구성 된 BGP 피어를 열거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d29e-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="6d29e-107">각 피어의 상태도 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d29e-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="6d29e-108">예제의</span><span class="sxs-lookup"><span data-stu-id="6d29e-108">EXAMPLES</span></span>

### <span data-ttu-id="6d29e-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="6d29e-109">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayBgpPeerStatus -ResourceGroupName resourceGroup -VirtualNetworkGatewayName gatewayName

Asn               : 65515
ConnectedDuration : 9.01:04:53.5768637
LocalAddress      : 10.1.0.254
MessagesReceived  : 14893
MessagesSent      : 14900
Neighbor          : 10.0.0.254
RoutesReceived    : 1
State             : Connected
```

<span data-ttu-id="6d29e-110">리소스 그룹 리소스 \에 있는 게이트웨이 이름 이라는 Azure 가상 네트워크 게이트웨이의 BGP 피어를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d29e-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>

<span data-ttu-id="6d29e-111">이 예제 출력에서는 10.0.0.254의 IP를 사용 하 여 연결 된 BGP 피어 하나를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6d29e-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="6d29e-112">변수</span><span class="sxs-lookup"><span data-stu-id="6d29e-112">PARAMETERS</span></span>

### <span data-ttu-id="6d29e-113">-투-피어</span><span class="sxs-lookup"><span data-stu-id="6d29e-113">-Peer</span></span>
<span data-ttu-id="6d29e-114">상태를 검색할 피어의 IP</span><span class="sxs-lookup"><span data-stu-id="6d29e-114">IP of the peer to retrieve status for</span></span>

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

### <span data-ttu-id="6d29e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d29e-115">-ResourceGroupName</span></span>
<span data-ttu-id="6d29e-116">가상 네트워크 게이트웨이 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="6d29e-116">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="6d29e-117">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="6d29e-117">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="6d29e-118">가상 네트워크 게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="6d29e-118">Virtual network gateway name</span></span>

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

### <span data-ttu-id="6d29e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d29e-119">-DefaultProfile</span></span>
<span data-ttu-id="6d29e-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d29e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d29e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d29e-121">CommonParameters</span></span>
<span data-ttu-id="6d29e-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d29e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d29e-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d29e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d29e-124">입력</span><span class="sxs-lookup"><span data-stu-id="6d29e-124">INPUTS</span></span>

### <span data-ttu-id="6d29e-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6d29e-125">System.String</span></span>

## <span data-ttu-id="6d29e-126">출력</span><span class="sxs-lookup"><span data-stu-id="6d29e-126">OUTPUTS</span></span>

### <span data-ttu-id="6d29e-127">PSBGPPeerStatus [] (으)로</span><span class="sxs-lookup"><span data-stu-id="6d29e-127">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus[]</span></span>

## <span data-ttu-id="6d29e-128">상속자</span><span class="sxs-lookup"><span data-stu-id="6d29e-128">NOTES</span></span>

## <span data-ttu-id="6d29e-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d29e-129">RELATED LINKS</span></span>

