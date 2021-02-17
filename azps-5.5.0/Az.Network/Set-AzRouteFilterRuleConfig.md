---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: eb8de50aac1b68928d5cebe8118665b9a24e8fbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191620"
---
# <span data-ttu-id="b2d72-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b2d72-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="b2d72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2d72-102">SYNOPSIS</span></span>
<span data-ttu-id="b2d72-103">경로 필터의 경로 필터 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2d72-103">Modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="b2d72-104">구문</span><span class="sxs-lookup"><span data-stu-id="b2d72-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2d72-105">설명</span><span class="sxs-lookup"><span data-stu-id="b2d72-105">DESCRIPTION</span></span>
<span data-ttu-id="b2d72-106">**Set-AzRouteFilterRuleConfig** cmdlet은 경로 필터의 경로 필터 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2d72-106">The **Set-AzRouteFilterRuleConfig** cmdlet modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="b2d72-107">예제</span><span class="sxs-lookup"><span data-stu-id="b2d72-107">EXAMPLES</span></span>

### <span data-ttu-id="b2d72-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b2d72-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> $rf = Set-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01" -Access Deny -RouteFilterRuleType Community -CommunityList "12076:5010","12076:5040"
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="b2d72-109">첫 번째 명령은 RouteFilter01이라는 경로 필터를 $rf 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b2d72-109">The first command gets the route filter named RouteFilter01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="b2d72-110">두 번째 명령은 Rule01이라는 경로 필터 규칙을 수정하고 업데이트된 경로 필터를 $rf 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b2d72-110">The second command modifies the route filter rule named Rule01 and stores updated route filter in the $rf variable.</span></span>
<span data-ttu-id="b2d72-111">세 번째 명령은 업데이트된 경로 필터를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b2d72-111">The third command saves updated route filter.</span></span>

## <span data-ttu-id="b2d72-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2d72-112">PARAMETERS</span></span>

### <span data-ttu-id="b2d72-113">-Access</span><span class="sxs-lookup"><span data-stu-id="b2d72-113">-Access</span></span>
<span data-ttu-id="b2d72-114">규칙의 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="b2d72-114">The access type of the rule.</span></span>
<span data-ttu-id="b2d72-115">가능한 값은 'Allow', 'Deny'입니다.</span><span class="sxs-lookup"><span data-stu-id="b2d72-115">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="b2d72-116">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="b2d72-116">-CommunityList</span></span>
<span data-ttu-id="b2d72-117">경로 필터가 필터링할 커뮤니티 값 목록</span><span class="sxs-lookup"><span data-stu-id="b2d72-117">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="b2d72-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2d72-118">-DefaultProfile</span></span>
<span data-ttu-id="b2d72-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2d72-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2d72-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b2d72-120">-Force</span></span>
<span data-ttu-id="b2d72-121">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2d72-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b2d72-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b2d72-122">-Name</span></span>
<span data-ttu-id="b2d72-123">경로 필터 규칙의 이름</span><span class="sxs-lookup"><span data-stu-id="b2d72-123">The name of the route filter rule</span></span>

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

### <span data-ttu-id="b2d72-124">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b2d72-124">-RouteFilter</span></span>
<span data-ttu-id="b2d72-125">The RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b2d72-125">The RouteFilter</span></span>

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

### <span data-ttu-id="b2d72-126">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="b2d72-126">-RouteFilterRuleType</span></span>
<span data-ttu-id="b2d72-127">규칙의 경로 필터 규칙 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="b2d72-127">The route filter rule type of the rule.</span></span>
<span data-ttu-id="b2d72-128">가능한 값은 'Community'입니다.</span><span class="sxs-lookup"><span data-stu-id="b2d72-128">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="b2d72-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2d72-129">-Confirm</span></span>
<span data-ttu-id="b2d72-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2d72-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2d72-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2d72-131">-WhatIf</span></span>
<span data-ttu-id="b2d72-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b2d72-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2d72-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2d72-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2d72-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d72-134">CommonParameters</span></span>
<span data-ttu-id="b2d72-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b2d72-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2d72-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b2d72-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d72-137">입력</span><span class="sxs-lookup"><span data-stu-id="b2d72-137">INPUTS</span></span>

### <span data-ttu-id="b2d72-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b2d72-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b2d72-139">출력</span><span class="sxs-lookup"><span data-stu-id="b2d72-139">OUTPUTS</span></span>

### <span data-ttu-id="b2d72-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b2d72-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b2d72-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b2d72-141">NOTES</span></span>

## <span data-ttu-id="b2d72-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2d72-142">RELATED LINKS</span></span>

[<span data-ttu-id="b2d72-143">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b2d72-143">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b2d72-144">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b2d72-144">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b2d72-145">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b2d72-145">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b2d72-146">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b2d72-146">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b2d72-147">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b2d72-147">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="b2d72-148">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b2d72-148">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="b2d72-149">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b2d72-149">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="b2d72-150">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b2d72-150">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
