---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azstaticroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
ms.openlocfilehash: e4d9b8cd09aa1bf1528de1cd2179a76e7907e82b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385393"
---
# <span data-ttu-id="4a3b1-101">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="4a3b1-101">New-AzStaticRoute</span></span>

## <span data-ttu-id="4a3b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a3b1-102">SYNOPSIS</span></span>
<span data-ttu-id="4a3b1-103">그런 다음 RoutingConfiguration 개체에 추가할 수 있는 StaticRoute 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4a3b1-103">Creates a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="4a3b1-104">구문</span><span class="sxs-lookup"><span data-stu-id="4a3b1-104">SYNTAX</span></span>

```powershell
New-AzStaticRoute -Name <String> -AddressPrefix <String[]> -NextHopIpAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a3b1-105">설명</span><span class="sxs-lookup"><span data-stu-id="4a3b1-105">DESCRIPTION</span></span>
<span data-ttu-id="4a3b1-106">StaticRoute 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4a3b1-106">Creates a StaticRoute object.</span></span>

## <span data-ttu-id="4a3b1-107">예제</span><span class="sxs-lookup"><span data-stu-id="4a3b1-107">EXAMPLES</span></span>

### <span data-ttu-id="4a3b1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4a3b1-108">Example 1</span></span>
```powershell
PS C:\> New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16") -NextHopIpAddress "10.90.0.5"

Name   AddressPrefixes              NextHopIpAddress
----   ---------------              ----------------
route1 {10.20.0.0/16, 10.30.0.0/16} 10.90.0.5
```

<span data-ttu-id="4a3b1-109">위의 명령은 StaticRoute 개체를 만든 다음 RoutingConfiguration 개체에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a3b1-109">The above command will create a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="4a3b1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a3b1-110">PARAMETERS</span></span>

### <span data-ttu-id="4a3b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a3b1-111">-DefaultProfile</span></span>
<span data-ttu-id="4a3b1-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a3b1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a3b1-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4a3b1-113">-AddressPrefix</span></span>
<span data-ttu-id="4a3b1-114">주소 연결선 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="4a3b1-114">List of address prefixes.</span></span>

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

### <span data-ttu-id="4a3b1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4a3b1-115">-Name</span></span>
<span data-ttu-id="4a3b1-116">경로 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a3b1-116">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3b1-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="4a3b1-117">-NextHopIpAddress</span></span>
<span data-ttu-id="4a3b1-118">다음 홉 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="4a3b1-118">The next hop ip address.</span></span>

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

### <span data-ttu-id="4a3b1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a3b1-119">CommonParameters</span></span>
<span data-ttu-id="4a3b1-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4a3b1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a3b1-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4a3b1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a3b1-122">입력</span><span class="sxs-lookup"><span data-stu-id="4a3b1-122">INPUTS</span></span>

### <span data-ttu-id="4a3b1-123">System.String</span><span class="sxs-lookup"><span data-stu-id="4a3b1-123">System.String</span></span>

## <span data-ttu-id="4a3b1-124">출력</span><span class="sxs-lookup"><span data-stu-id="4a3b1-124">OUTPUTS</span></span>

### <span data-ttu-id="4a3b1-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="4a3b1-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="4a3b1-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4a3b1-126">NOTES</span></span>

## <span data-ttu-id="4a3b1-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a3b1-127">RELATED LINKS</span></span>

[<span data-ttu-id="4a3b1-128">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a3b1-128">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
