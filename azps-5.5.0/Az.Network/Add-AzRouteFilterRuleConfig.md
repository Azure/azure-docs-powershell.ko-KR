---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 204ecf05f0781649f441399c7a9b6acfbfbd8cdd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192020"
---
# <span data-ttu-id="2af84-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2af84-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="2af84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2af84-102">SYNOPSIS</span></span>
<span data-ttu-id="2af84-103">경로 필터에 경로 필터 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2af84-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="2af84-104">구문</span><span class="sxs-lookup"><span data-stu-id="2af84-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2af84-105">설명</span><span class="sxs-lookup"><span data-stu-id="2af84-105">DESCRIPTION</span></span>
<span data-ttu-id="2af84-106">Add-AzRouteFilterRuleConfig cmdlet은 Azure 경로 필터에 경로 필터 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2af84-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="2af84-107">예제</span><span class="sxs-lookup"><span data-stu-id="2af84-107">EXAMPLES</span></span>

### <span data-ttu-id="2af84-108">예제 1: 경로 필터에 경로 필터 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="2af84-108">Example 1: Add a route filter rule to a route filter</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="2af84-109">첫 번째 명령은 Get-AzRouteFilter cmdlet을 사용하여 routefilter01이라는 경로 필터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2af84-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="2af84-110">이 명령은 필터를 $RouteFilter 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="2af84-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="2af84-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2af84-111">PARAMETERS</span></span>

### <span data-ttu-id="2af84-112">-Access</span><span class="sxs-lookup"><span data-stu-id="2af84-112">-Access</span></span>
<span data-ttu-id="2af84-113">경로 필터 규칙의 액세스를 지정하고 유효한 값은 거부 또는 허용입니다.</span><span class="sxs-lookup"><span data-stu-id="2af84-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2af84-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="2af84-114">-CommunityList</span></span>
<span data-ttu-id="2af84-115">경로 필터가 필터링할 커뮤니티 값 목록</span><span class="sxs-lookup"><span data-stu-id="2af84-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="2af84-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2af84-116">-DefaultProfile</span></span>
<span data-ttu-id="2af84-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2af84-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2af84-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2af84-118">-Force</span></span>
<span data-ttu-id="2af84-119">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2af84-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2af84-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2af84-120">-Name</span></span>
<span data-ttu-id="2af84-121">경로 필터에 추가할 경로 필터 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2af84-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="2af84-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="2af84-122">-RouteFilter</span></span>
<span data-ttu-id="2af84-123">이 cmdlet에서 경로 필터 규칙을 추가하는 경로 필터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2af84-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2af84-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="2af84-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="2af84-125">경로 필터 규칙 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2af84-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="2af84-126">유효한 값은 커뮤니티입니다.</span><span class="sxs-lookup"><span data-stu-id="2af84-126">Valid values are: Community</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2af84-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2af84-127">-Confirm</span></span>
<span data-ttu-id="2af84-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2af84-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2af84-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2af84-129">-WhatIf</span></span>
<span data-ttu-id="2af84-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2af84-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2af84-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2af84-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2af84-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2af84-132">CommonParameters</span></span>
<span data-ttu-id="2af84-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2af84-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2af84-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2af84-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2af84-135">입력</span><span class="sxs-lookup"><span data-stu-id="2af84-135">INPUTS</span></span>

### <span data-ttu-id="2af84-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2af84-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="2af84-137">출력</span><span class="sxs-lookup"><span data-stu-id="2af84-137">OUTPUTS</span></span>

### <span data-ttu-id="2af84-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2af84-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="2af84-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2af84-139">NOTES</span></span>
<span data-ttu-id="2af84-140">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="2af84-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="2af84-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2af84-141">RELATED LINKS</span></span>

[<span data-ttu-id="2af84-142">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2af84-142">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2af84-143">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2af84-143">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2af84-144">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2af84-144">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2af84-145">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2af84-145">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="2af84-146">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2af84-146">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="2af84-147">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2af84-147">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="2af84-148">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2af84-148">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="2af84-149">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2af84-149">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
