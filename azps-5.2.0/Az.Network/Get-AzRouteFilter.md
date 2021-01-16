---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 88b755a8865a5ce07a5dc86c94958de0c0e72485
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341378"
---
# <span data-ttu-id="db1bd-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="db1bd-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="db1bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db1bd-102">SYNOPSIS</span></span>
<span data-ttu-id="db1bd-103">경로 필터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="db1bd-103">Gets a route filter.</span></span>

## <span data-ttu-id="db1bd-104">구문</span><span class="sxs-lookup"><span data-stu-id="db1bd-104">SYNTAX</span></span>

### <span data-ttu-id="db1bd-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="db1bd-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db1bd-106">확장</span><span class="sxs-lookup"><span data-stu-id="db1bd-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db1bd-107">설명</span><span class="sxs-lookup"><span data-stu-id="db1bd-107">DESCRIPTION</span></span>
<span data-ttu-id="db1bd-108">**Get-AzRouteFilter** cmdlet은 경로 필터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="db1bd-108">The **Get-AzRouteFilter** cmdlet gets a route filter.</span></span>

## <span data-ttu-id="db1bd-109">예제</span><span class="sxs-lookup"><span data-stu-id="db1bd-109">EXAMPLES</span></span>

### <span data-ttu-id="db1bd-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="db1bd-110">Example 1</span></span>
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

<span data-ttu-id="db1bd-111">이 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 RouteFilter01이라는 경로 필터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="db1bd-111">This command gets the route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="db1bd-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="db1bd-112">Example 2</span></span>
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

<span data-ttu-id="db1bd-113">이 명령은 "RouteFilter"로 시작하는 모든 경로 필터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="db1bd-113">This command gets all route filters that start with "RouteFilter".</span></span>

## <span data-ttu-id="db1bd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db1bd-114">PARAMETERS</span></span>

### <span data-ttu-id="db1bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db1bd-115">-DefaultProfile</span></span>
<span data-ttu-id="db1bd-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db1bd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db1bd-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="db1bd-117">-ExpandResource</span></span>
<span data-ttu-id="db1bd-118">확장할 리소스 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="db1bd-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="db1bd-119">-Name</span><span class="sxs-lookup"><span data-stu-id="db1bd-119">-Name</span></span>
<span data-ttu-id="db1bd-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db1bd-120">The resource name.</span></span>

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

### <span data-ttu-id="db1bd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db1bd-121">-ResourceGroupName</span></span>
<span data-ttu-id="db1bd-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db1bd-122">The resource group name.</span></span>

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

### <span data-ttu-id="db1bd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db1bd-123">CommonParameters</span></span>
<span data-ttu-id="db1bd-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="db1bd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db1bd-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="db1bd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db1bd-126">입력</span><span class="sxs-lookup"><span data-stu-id="db1bd-126">INPUTS</span></span>

### <span data-ttu-id="db1bd-127">System.String</span><span class="sxs-lookup"><span data-stu-id="db1bd-127">System.String</span></span>

## <span data-ttu-id="db1bd-128">출력</span><span class="sxs-lookup"><span data-stu-id="db1bd-128">OUTPUTS</span></span>

### <span data-ttu-id="db1bd-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="db1bd-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="db1bd-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="db1bd-130">NOTES</span></span>

## <span data-ttu-id="db1bd-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db1bd-131">RELATED LINKS</span></span>

[<span data-ttu-id="db1bd-132">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="db1bd-132">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="db1bd-133">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="db1bd-133">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="db1bd-134">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="db1bd-134">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="db1bd-135">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="db1bd-135">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="db1bd-136">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="db1bd-136">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="db1bd-137">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="db1bd-137">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="db1bd-138">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="db1bd-138">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="db1bd-139">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="db1bd-139">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
