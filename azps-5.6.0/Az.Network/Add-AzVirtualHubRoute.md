---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: d90d25776f895bee47549dfb08a4588f0e446883
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979755"
---
# <span data-ttu-id="a6f70-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="a6f70-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="a6f70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6f70-102">SYNOPSIS</span></span>
<span data-ttu-id="a6f70-103">가상HubRoute 개체를 만듭니다. 이 개체를 매개 변수로 전달할 Add-AzVirtualHubRouteTable 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6f70-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="a6f70-104">구문</span><span class="sxs-lookup"><span data-stu-id="a6f70-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6f70-105">설명</span><span class="sxs-lookup"><span data-stu-id="a6f70-105">DESCRIPTION</span></span>
<span data-ttu-id="a6f70-106">VirtualHubRoute 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a6f70-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="a6f70-107">예제</span><span class="sxs-lookup"><span data-stu-id="a6f70-107">EXAMPLES</span></span>

### <span data-ttu-id="a6f70-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a6f70-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="a6f70-109">위의 명령은 VirtualHubRoute 개체를 만든 다음 VirtualHubRouteTable 리소스에 추가하고 VirtualHub로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6f70-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="a6f70-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a6f70-110">PARAMETERS</span></span>

### <span data-ttu-id="a6f70-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6f70-111">-DefaultProfile</span></span>
<span data-ttu-id="a6f70-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6f70-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6f70-113">-대상</span><span class="sxs-lookup"><span data-stu-id="a6f70-113">-Destination</span></span>
<span data-ttu-id="a6f70-114">대상 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a6f70-114">List of Destinations.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f70-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="a6f70-115">-DestinationType</span></span>
<span data-ttu-id="a6f70-116">대상 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a6f70-116">Type of Destinations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f70-117">-NextHop</span><span class="sxs-lookup"><span data-stu-id="a6f70-117">-NextHop</span></span>
<span data-ttu-id="a6f70-118">다음 홉 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a6f70-118">List of Next hops.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f70-119">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="a6f70-119">-NextHopType</span></span>
<span data-ttu-id="a6f70-120">다음 홉 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a6f70-120">The Next Hop type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f70-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6f70-121">CommonParameters</span></span>
<span data-ttu-id="a6f70-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a6f70-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6f70-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6f70-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6f70-124">입력</span><span class="sxs-lookup"><span data-stu-id="a6f70-124">INPUTS</span></span>

### <span data-ttu-id="a6f70-125">없음</span><span class="sxs-lookup"><span data-stu-id="a6f70-125">None</span></span>

## <span data-ttu-id="a6f70-126">출력</span><span class="sxs-lookup"><span data-stu-id="a6f70-126">OUTPUTS</span></span>

### <span data-ttu-id="a6f70-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="a6f70-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="a6f70-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a6f70-128">NOTES</span></span>

## <span data-ttu-id="a6f70-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6f70-129">RELATED LINKS</span></span>
