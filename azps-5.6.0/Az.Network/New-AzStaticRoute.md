---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azstaticroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
ms.openlocfilehash: 2cf661ab2bcc531c0a88ae86934a53b212bb91d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953776"
---
# <span data-ttu-id="f8cb6-101">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="f8cb6-101">New-AzStaticRoute</span></span>

## <span data-ttu-id="f8cb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="f8cb6-103">그런 다음 라우팅 구성 개체에 추가할 수 있는 StaticRoute 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-103">Creates a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="f8cb6-104">구문</span><span class="sxs-lookup"><span data-stu-id="f8cb6-104">SYNTAX</span></span>

```powershell
New-AzStaticRoute -Name <String> -AddressPrefix <String[]> -NextHopIpAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8cb6-105">설명</span><span class="sxs-lookup"><span data-stu-id="f8cb6-105">DESCRIPTION</span></span>
<span data-ttu-id="f8cb6-106">StaticRoute 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-106">Creates a StaticRoute object.</span></span>

## <span data-ttu-id="f8cb6-107">예제</span><span class="sxs-lookup"><span data-stu-id="f8cb6-107">EXAMPLES</span></span>

### <span data-ttu-id="f8cb6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f8cb6-108">Example 1</span></span>
```powershell
PS C:\> New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16") -NextHopIpAddress "10.90.0.5"

Name   AddressPrefixes              NextHopIpAddress
----   ---------------              ----------------
route1 {10.20.0.0/16, 10.30.0.0/16} 10.90.0.5
```

<span data-ttu-id="f8cb6-109">위의 명령은 StaticRoute 개체를 만든 다음 라우팅Configuration 개체에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-109">The above command will create a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="f8cb6-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f8cb6-110">PARAMETERS</span></span>

### <span data-ttu-id="f8cb6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8cb6-111">-DefaultProfile</span></span>
<span data-ttu-id="f8cb6-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8cb6-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f8cb6-113">-AddressPrefix</span></span>
<span data-ttu-id="f8cb6-114">주소 연결선 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-114">List of address prefixes.</span></span>

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

### <span data-ttu-id="f8cb6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f8cb6-115">-Name</span></span>
<span data-ttu-id="f8cb6-116">경로 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-116">The route name.</span></span>

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

### <span data-ttu-id="f8cb6-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="f8cb6-117">-NextHopIpAddress</span></span>
<span data-ttu-id="f8cb6-118">다음 홉 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-118">The next hop ip address.</span></span>

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

### <span data-ttu-id="f8cb6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8cb6-119">CommonParameters</span></span>
<span data-ttu-id="f8cb6-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8cb6-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8cb6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8cb6-122">입력</span><span class="sxs-lookup"><span data-stu-id="f8cb6-122">INPUTS</span></span>

### <span data-ttu-id="f8cb6-123">System.String</span><span class="sxs-lookup"><span data-stu-id="f8cb6-123">System.String</span></span>

## <span data-ttu-id="f8cb6-124">출력</span><span class="sxs-lookup"><span data-stu-id="f8cb6-124">OUTPUTS</span></span>

### <span data-ttu-id="f8cb6-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="f8cb6-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="f8cb6-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f8cb6-126">NOTES</span></span>

## <span data-ttu-id="f8cb6-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8cb6-127">RELATED LINKS</span></span>

[<span data-ttu-id="f8cb6-128">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8cb6-128">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
