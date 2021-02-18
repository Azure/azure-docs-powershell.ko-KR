---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: 84a1de629e983e78531faa9f33c33f43df4c5372
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184780"
---
# <span data-ttu-id="8aca1-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="8aca1-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="8aca1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8aca1-102">SYNOPSIS</span></span>
<span data-ttu-id="8aca1-103">가상 머신 명령에 매개 변수로 전달될 수 있는 VirtualHubRoute Add-AzVirtualHubRouteTable 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8aca1-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="8aca1-104">구문</span><span class="sxs-lookup"><span data-stu-id="8aca1-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8aca1-105">설명</span><span class="sxs-lookup"><span data-stu-id="8aca1-105">DESCRIPTION</span></span>
<span data-ttu-id="8aca1-106">VirtualHubRoute 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8aca1-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="8aca1-107">예제</span><span class="sxs-lookup"><span data-stu-id="8aca1-107">EXAMPLES</span></span>

### <span data-ttu-id="8aca1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8aca1-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="8aca1-109">위의 명령은 VirtualHubRouteTable 리소스에 추가하고 VirtualHub로 설정할 수 있는 VirtualHubRoute 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8aca1-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="8aca1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8aca1-110">PARAMETERS</span></span>

### <span data-ttu-id="8aca1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aca1-111">-DefaultProfile</span></span>
<span data-ttu-id="8aca1-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8aca1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8aca1-113">-Destination</span><span class="sxs-lookup"><span data-stu-id="8aca1-113">-Destination</span></span>
<span data-ttu-id="8aca1-114">대상 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="8aca1-114">List of Destinations.</span></span>

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

### <span data-ttu-id="8aca1-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="8aca1-115">-DestinationType</span></span>
<span data-ttu-id="8aca1-116">대상 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="8aca1-116">Type of Destinations.</span></span>

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

### <span data-ttu-id="8aca1-117">-NextHop</span><span class="sxs-lookup"><span data-stu-id="8aca1-117">-NextHop</span></span>
<span data-ttu-id="8aca1-118">다음 홉 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="8aca1-118">List of Next hops.</span></span>

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

### <span data-ttu-id="8aca1-119">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="8aca1-119">-NextHopType</span></span>
<span data-ttu-id="8aca1-120">다음 홉 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="8aca1-120">The Next Hop type.</span></span>

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

### <span data-ttu-id="8aca1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aca1-121">CommonParameters</span></span>
<span data-ttu-id="8aca1-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8aca1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aca1-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8aca1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aca1-124">입력</span><span class="sxs-lookup"><span data-stu-id="8aca1-124">INPUTS</span></span>

### <span data-ttu-id="8aca1-125">없음</span><span class="sxs-lookup"><span data-stu-id="8aca1-125">None</span></span>

## <span data-ttu-id="8aca1-126">출력</span><span class="sxs-lookup"><span data-stu-id="8aca1-126">OUTPUTS</span></span>

### <span data-ttu-id="8aca1-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="8aca1-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="8aca1-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8aca1-128">NOTES</span></span>

## <span data-ttu-id="8aca1-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8aca1-129">RELATED LINKS</span></span>
