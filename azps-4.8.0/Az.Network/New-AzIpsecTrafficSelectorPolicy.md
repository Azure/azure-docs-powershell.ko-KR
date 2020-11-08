---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsectrafficselectorpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
ms.openlocfilehash: f335272bce6591c617d8111dd1d0d81af50ec255
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211568"
---
# <span data-ttu-id="8b21f-101">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="8b21f-101">New-AzIpsecTrafficSelectorPolicy</span></span>

## <span data-ttu-id="8b21f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b21f-102">SYNOPSIS</span></span>
<span data-ttu-id="8b21f-103">트래픽 선택기 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b21f-103">Creates a traffic selector policy.</span></span>

## <span data-ttu-id="8b21f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8b21f-104">SYNTAX</span></span>

```
New-AzIpsecTrafficSelectorPolicy -LocalAddressRange <String[]> -RemoteAddressRange <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b21f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8b21f-105">DESCRIPTION</span></span>
<span data-ttu-id="8b21f-106">New-AzTrafficSelectorPolicy cmdlet은 가상 네트워크 게이트웨이 연결에 사용 되는 트래픽 선택기 정책 제안을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b21f-106">The New-AzTrafficSelectorPolicy cmdlet creates a traffic selector policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="8b21f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8b21f-107">EXAMPLES</span></span>

### <span data-ttu-id="8b21f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8b21f-108">Example 1</span></span>
```powershell
$trafficSelectorPolicy = New-AzIpsecTrafficSelectorPolicy -LocalAddressRange ("10.10.10.0/24", "20.20.20.0/24") -RemoteAddressRange ("30.30.30.0/24", "40.40.40.0/24")
New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -TrafficSelectorPolicies ($trafficSelectorPolicy)
```

<span data-ttu-id="8b21f-109">IKEv2 프로토콜을 사용 하 여 가상 네트워크 게이트웨이 연결을 만들 때 트래픽 선택기 정책의 인스턴스를 만들고이를 매개 변수로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b21f-109">Creates an instance of a traffic selector policy and adds it as a parameter when creating a virtual network gateway connection with an IKEv2 protocol.</span></span>

## <span data-ttu-id="8b21f-110">변수</span><span class="sxs-lookup"><span data-stu-id="8b21f-110">PARAMETERS</span></span>

### <span data-ttu-id="8b21f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b21f-111">-DefaultProfile</span></span>
<span data-ttu-id="8b21f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b21f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b21f-113">-LocalAddressRange</span><span class="sxs-lookup"><span data-stu-id="8b21f-113">-LocalAddressRange</span></span>
<span data-ttu-id="8b21f-114">CIDR 주소 범위의 모음</span><span class="sxs-lookup"><span data-stu-id="8b21f-114">A collection of CIDR address ranges</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b21f-115">-RemoteAddressRange</span><span class="sxs-lookup"><span data-stu-id="8b21f-115">-RemoteAddressRange</span></span>
<span data-ttu-id="8b21f-116">CIDR 주소 범위의 모음</span><span class="sxs-lookup"><span data-stu-id="8b21f-116">A collection of CIDR address ranges</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b21f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b21f-117">CommonParameters</span></span>
<span data-ttu-id="8b21f-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b21f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b21f-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8b21f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b21f-120">입력</span><span class="sxs-lookup"><span data-stu-id="8b21f-120">INPUTS</span></span>

### <span data-ttu-id="8b21f-121">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="8b21f-121">System.String[]</span></span>

## <span data-ttu-id="8b21f-122">출력</span><span class="sxs-lookup"><span data-stu-id="8b21f-122">OUTPUTS</span></span>

### <span data-ttu-id="8b21f-123">PSTrafficSelectorPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8b21f-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span></span>

## <span data-ttu-id="8b21f-124">상속자</span><span class="sxs-lookup"><span data-stu-id="8b21f-124">NOTES</span></span>

## <span data-ttu-id="8b21f-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b21f-125">RELATED LINKS</span></span>
