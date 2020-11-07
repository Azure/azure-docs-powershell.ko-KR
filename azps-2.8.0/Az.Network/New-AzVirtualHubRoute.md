---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: 8a9184eddaf5b614b4338a95e1d895d645e0832e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869841"
---
# <span data-ttu-id="521ae-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="521ae-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="521ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="521ae-102">SYNOPSIS</span></span>
<span data-ttu-id="521ae-103">Azure 가상 허브 경로 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="521ae-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="521ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="521ae-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="521ae-105">설명은</span><span class="sxs-lookup"><span data-stu-id="521ae-105">DESCRIPTION</span></span>
<span data-ttu-id="521ae-106">Azure 가상 허브 경로 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="521ae-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="521ae-107">예제의</span><span class="sxs-lookup"><span data-stu-id="521ae-107">EXAMPLES</span></span>

### <span data-ttu-id="521ae-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="521ae-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="521ae-109">위의 방법을 통해 가상 허브 경로 테이블에 포함할 수 있는 가상 허브 경로 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="521ae-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="521ae-110">가상 허브 경로는 VirtualHubRouteTable 개체를 만드는 데 사용할 수 있는 메모리 내 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="521ae-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="521ae-111">변수</span><span class="sxs-lookup"><span data-stu-id="521ae-111">PARAMETERS</span></span>

### <span data-ttu-id="521ae-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="521ae-112">-AddressPrefix</span></span>
<span data-ttu-id="521ae-113">주소 접두사 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="521ae-113">List of Address Prefixes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="521ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="521ae-114">-DefaultProfile</span></span>
<span data-ttu-id="521ae-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="521ae-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="521ae-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="521ae-116">-NextHopIpAddress</span></span>
<span data-ttu-id="521ae-117">다음 홉 IpAddress.</span><span class="sxs-lookup"><span data-stu-id="521ae-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="521ae-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="521ae-118">CommonParameters</span></span>
<span data-ttu-id="521ae-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="521ae-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="521ae-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="521ae-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="521ae-121">입력</span><span class="sxs-lookup"><span data-stu-id="521ae-121">INPUTS</span></span>

### <span data-ttu-id="521ae-122">않아야</span><span class="sxs-lookup"><span data-stu-id="521ae-122">None</span></span>

## <span data-ttu-id="521ae-123">출력</span><span class="sxs-lookup"><span data-stu-id="521ae-123">OUTPUTS</span></span>

### <span data-ttu-id="521ae-124">PSVirtualHubRoute에 대 한.</span><span class="sxs-lookup"><span data-stu-id="521ae-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="521ae-125">상속자</span><span class="sxs-lookup"><span data-stu-id="521ae-125">NOTES</span></span>

## <span data-ttu-id="521ae-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="521ae-126">RELATED LINKS</span></span>

[<span data-ttu-id="521ae-127">새로운 AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="521ae-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)
