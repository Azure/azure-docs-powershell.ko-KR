---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: 84a1de629e983e78531faa9f33c33f43df4c5372
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042541"
---
# <span data-ttu-id="20556-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="20556-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="20556-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20556-102">SYNOPSIS</span></span>
<span data-ttu-id="20556-103">Add-AzVirtualHubRouteTable 명령에 매개 변수로 전달 될 수 있는 VirtualHubRoute 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20556-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="20556-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20556-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20556-105">설명은</span><span class="sxs-lookup"><span data-stu-id="20556-105">DESCRIPTION</span></span>
<span data-ttu-id="20556-106">VirtualHubRoute 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20556-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="20556-107">예제의</span><span class="sxs-lookup"><span data-stu-id="20556-107">EXAMPLES</span></span>

### <span data-ttu-id="20556-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="20556-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="20556-109">위 명령에서는 VirtualHubRouteTable 리소스에 추가 하 고 VirtualHub로 설정할 수 있는 VirtualHubRoute 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20556-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="20556-110">변수</span><span class="sxs-lookup"><span data-stu-id="20556-110">PARAMETERS</span></span>

### <span data-ttu-id="20556-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20556-111">-DefaultProfile</span></span>
<span data-ttu-id="20556-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20556-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20556-113">-대상</span><span class="sxs-lookup"><span data-stu-id="20556-113">-Destination</span></span>
<span data-ttu-id="20556-114">대상의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="20556-114">List of Destinations.</span></span>

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

### <span data-ttu-id="20556-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="20556-115">-DestinationType</span></span>
<span data-ttu-id="20556-116">대상의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="20556-116">Type of Destinations.</span></span>

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

### <span data-ttu-id="20556-117">-NextHop</span><span class="sxs-lookup"><span data-stu-id="20556-117">-NextHop</span></span>
<span data-ttu-id="20556-118">다음 홉의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="20556-118">List of Next hops.</span></span>

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

### <span data-ttu-id="20556-119">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="20556-119">-NextHopType</span></span>
<span data-ttu-id="20556-120">다음 홉 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="20556-120">The Next Hop type.</span></span>

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

### <span data-ttu-id="20556-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20556-121">CommonParameters</span></span>
<span data-ttu-id="20556-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20556-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20556-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="20556-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20556-124">입력</span><span class="sxs-lookup"><span data-stu-id="20556-124">INPUTS</span></span>

### <span data-ttu-id="20556-125">않아야</span><span class="sxs-lookup"><span data-stu-id="20556-125">None</span></span>

## <span data-ttu-id="20556-126">출력</span><span class="sxs-lookup"><span data-stu-id="20556-126">OUTPUTS</span></span>

### <span data-ttu-id="20556-127">PSVirtualHubRoute에 대 한.</span><span class="sxs-lookup"><span data-stu-id="20556-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="20556-128">상속자</span><span class="sxs-lookup"><span data-stu-id="20556-128">NOTES</span></span>

## <span data-ttu-id="20556-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20556-129">RELATED LINKS</span></span>
