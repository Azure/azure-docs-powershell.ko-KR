---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: 288a2382470682c8c7b55f7342d5a0f193446019
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537968"
---
# <span data-ttu-id="49409-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="49409-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="49409-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49409-102">SYNOPSIS</span></span>
<span data-ttu-id="49409-103">Azure 가상 네트워크 게이트웨이에서 광고 하는 경로를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="49409-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49409-104">구문과</span><span class="sxs-lookup"><span data-stu-id="49409-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49409-105">설명은</span><span class="sxs-lookup"><span data-stu-id="49409-105">DESCRIPTION</span></span>
<span data-ttu-id="49409-106">BGP 피어의 IP가 주어진 경우 지정 된 Azure 가상 네트워크 게이트웨이에서 해당 피어에 알린 경로를 열거 합니다.</span><span class="sxs-lookup"><span data-stu-id="49409-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="49409-107">예제의</span><span class="sxs-lookup"><span data-stu-id="49409-107">EXAMPLES</span></span>

### <span data-ttu-id="49409-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="49409-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="49409-109">리소스 그룹 resourceGroupName의 Azure gateway에 대 한 retrives Name에 대해 IP 10.0.0.254를 사용 하 여 BGP 피어에 알리는 경로 목록를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49409-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrives a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="49409-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="49409-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="49409-111">리소스 그룹 resourceGroupName의 Azure gateway의 게이트웨이 이름에 대해 게이트웨이에서 BGP 피어 목록의 첫 번째 BGP 피어에 알리는 경로를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="49409-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="49409-112">변수</span><span class="sxs-lookup"><span data-stu-id="49409-112">PARAMETERS</span></span>

### <span data-ttu-id="49409-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49409-113">-AsJob</span></span>
<span data-ttu-id="49409-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="49409-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49409-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49409-115">-DefaultProfile</span></span>
<span data-ttu-id="49409-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49409-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49409-117">-투-피어</span><span class="sxs-lookup"><span data-stu-id="49409-117">-Peer</span></span>
<span data-ttu-id="49409-118">BGP 피어의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="49409-118">BGP peer's IP address.</span></span> <span data-ttu-id="49409-119">이는 게이트웨이가 배포 된 Azure 가상 네트워크 내에서 액세스할 수 있는 주소 공간 내의 IP 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="49409-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="49409-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49409-120">-ResourceGroupName</span></span>
<span data-ttu-id="49409-121">가상 네트워크 게이트웨이 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="49409-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="49409-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="49409-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="49409-123">가상 네트워크 게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="49409-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="49409-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49409-124">CommonParameters</span></span>
<span data-ttu-id="49409-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="49409-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49409-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49409-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49409-127">입력</span><span class="sxs-lookup"><span data-stu-id="49409-127">INPUTS</span></span>

### <span data-ttu-id="49409-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="49409-128">System.String</span></span>

## <span data-ttu-id="49409-129">출력</span><span class="sxs-lookup"><span data-stu-id="49409-129">OUTPUTS</span></span>

### <span data-ttu-id="49409-130">Microsoft. Azure. Ps네트워크 경로</span><span class="sxs-lookup"><span data-stu-id="49409-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="49409-131">상속자</span><span class="sxs-lookup"><span data-stu-id="49409-131">NOTES</span></span>
<span data-ttu-id="49409-132">이 명령은 BGP 사용 연결이 있는 Azure 가상 네트워크 게이트웨이에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="49409-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="49409-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49409-133">RELATED LINKS</span></span>
