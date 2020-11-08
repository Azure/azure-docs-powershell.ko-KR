---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 88b755a8865a5ce07a5dc86c94958de0c0e72485
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204003"
---
# <span data-ttu-id="1cb2f-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1cb2f-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="1cb2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cb2f-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb2f-103">경로 필터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1cb2f-103">Gets a route filter.</span></span>

## <span data-ttu-id="1cb2f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1cb2f-104">SYNTAX</span></span>

### <span data-ttu-id="1cb2f-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="1cb2f-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1cb2f-106">확장</span><span class="sxs-lookup"><span data-stu-id="1cb2f-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cb2f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1cb2f-107">DESCRIPTION</span></span>
<span data-ttu-id="1cb2f-108">**Get-AzRouteFilter** cmdlet은 경로 필터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1cb2f-108">The **Get-AzRouteFilter** cmdlet gets a route filter.</span></span>

## <span data-ttu-id="1cb2f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1cb2f-109">EXAMPLES</span></span>

### <span data-ttu-id="1cb2f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1cb2f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"

Name              : RouteFilter01
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter01
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []
```

<span data-ttu-id="1cb2f-111">이 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 RouteFilter01 이라는 경로 필터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1cb2f-111">This command gets the route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="1cb2f-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="1cb2f-112">Example 2</span></span>
```powershell
PS C:\> Get-AzRouteFilter -Name "RouteFilter*"

Name              : RouteFilter01
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter01
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []

Name              : RouteFilter02
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter02
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []
```

<span data-ttu-id="1cb2f-113">이 명령은 "RouteFilter"로 시작 하는 모든 경로 필터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1cb2f-113">This command gets all route filters that start with "RouteFilter".</span></span>

## <span data-ttu-id="1cb2f-114">변수</span><span class="sxs-lookup"><span data-stu-id="1cb2f-114">PARAMETERS</span></span>

### <span data-ttu-id="1cb2f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb2f-115">-DefaultProfile</span></span>
<span data-ttu-id="1cb2f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb2f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cb2f-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="1cb2f-117">-ExpandResource</span></span>
<span data-ttu-id="1cb2f-118">확장할 리소스 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb2f-118">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb2f-119">-이름</span><span class="sxs-lookup"><span data-stu-id="1cb2f-119">-Name</span></span>
<span data-ttu-id="1cb2f-120">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb2f-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1cb2f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cb2f-121">-ResourceGroupName</span></span>
<span data-ttu-id="1cb2f-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb2f-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1cb2f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb2f-123">CommonParameters</span></span>
<span data-ttu-id="1cb2f-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cb2f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb2f-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1cb2f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb2f-126">입력</span><span class="sxs-lookup"><span data-stu-id="1cb2f-126">INPUTS</span></span>

### <span data-ttu-id="1cb2f-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1cb2f-127">System.String</span></span>

## <span data-ttu-id="1cb2f-128">출력</span><span class="sxs-lookup"><span data-stu-id="1cb2f-128">OUTPUTS</span></span>

### <span data-ttu-id="1cb2f-129">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="1cb2f-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1cb2f-130">상속자</span><span class="sxs-lookup"><span data-stu-id="1cb2f-130">NOTES</span></span>

## <span data-ttu-id="1cb2f-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1cb2f-131">RELATED LINKS</span></span>

[<span data-ttu-id="1cb2f-132">새로운 AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1cb2f-132">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="1cb2f-133">제거-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1cb2f-133">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="1cb2f-134">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1cb2f-134">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="1cb2f-135">추가-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1cb2f-135">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1cb2f-136">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1cb2f-136">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1cb2f-137">새로운 AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1cb2f-137">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1cb2f-138">제거-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1cb2f-138">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1cb2f-139">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1cb2f-139">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
