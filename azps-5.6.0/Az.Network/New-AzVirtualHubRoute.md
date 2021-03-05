---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: 42553004f8d084496a1f4809bca408e0b4c62cef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990024"
---
# <span data-ttu-id="73954-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="73954-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="73954-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73954-102">SYNOPSIS</span></span>
<span data-ttu-id="73954-103">Azure Virtual Hub 경로 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73954-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="73954-104">구문</span><span class="sxs-lookup"><span data-stu-id="73954-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73954-105">설명</span><span class="sxs-lookup"><span data-stu-id="73954-105">DESCRIPTION</span></span>
<span data-ttu-id="73954-106">Azure Virtual Hub 경로 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73954-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="73954-107">예제</span><span class="sxs-lookup"><span data-stu-id="73954-107">EXAMPLES</span></span>

### <span data-ttu-id="73954-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="73954-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="73954-109">위의 가상 허브 경로 테이블에 포함될 수 있는 가상 허브 경로 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73954-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="73954-110">가상 허브 경로는 VirtualHubRouteTable 개체를 만드는 데 사용할 수 있는 메모리 내 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="73954-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="73954-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="73954-111">PARAMETERS</span></span>

### <span data-ttu-id="73954-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="73954-112">-AddressPrefix</span></span>
<span data-ttu-id="73954-113">주소 연결선 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="73954-113">List of Address Prefixes.</span></span>

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

### <span data-ttu-id="73954-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73954-114">-DefaultProfile</span></span>
<span data-ttu-id="73954-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73954-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73954-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="73954-116">-NextHopIpAddress</span></span>
<span data-ttu-id="73954-117">다음 홉 IPAddress입니다.</span><span class="sxs-lookup"><span data-stu-id="73954-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="73954-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73954-118">CommonParameters</span></span>
<span data-ttu-id="73954-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73954-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73954-120">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="73954-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73954-121">입력</span><span class="sxs-lookup"><span data-stu-id="73954-121">INPUTS</span></span>

### <span data-ttu-id="73954-122">없음</span><span class="sxs-lookup"><span data-stu-id="73954-122">None</span></span>

## <span data-ttu-id="73954-123">출력</span><span class="sxs-lookup"><span data-stu-id="73954-123">OUTPUTS</span></span>

### <span data-ttu-id="73954-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="73954-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="73954-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="73954-125">NOTES</span></span>

## <span data-ttu-id="73954-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73954-126">RELATED LINKS</span></span>

[<span data-ttu-id="73954-127">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="73954-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)
