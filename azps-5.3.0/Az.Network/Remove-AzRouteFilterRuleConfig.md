---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: e596ea3092cd5fda045c20f80c9208015b57a42d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385274"
---
# <span data-ttu-id="39161-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39161-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="39161-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39161-102">SYNOPSIS</span></span>
<span data-ttu-id="39161-103">경로 필터에서 경로 필터 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="39161-103">Removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="39161-104">구문</span><span class="sxs-lookup"><span data-stu-id="39161-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39161-105">설명</span><span class="sxs-lookup"><span data-stu-id="39161-105">DESCRIPTION</span></span>
<span data-ttu-id="39161-106">**Remove-AzRouteFilterRuleConfig** cmdlet은 경로 필터에서 경로 필터 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="39161-106">The **Remove-AzRouteFilterRuleConfig** cmdlet removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="39161-107">예제</span><span class="sxs-lookup"><span data-stu-id="39161-107">EXAMPLES</span></span>

### <span data-ttu-id="39161-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="39161-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
```

<span data-ttu-id="39161-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 RouteFilter01이라는 경로 필터를 사용하여 $rf 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="39161-109">The first command gets a route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="39161-110">두 번째 명령은 규칙에 저장된 경로 필터에서 Rule01이라는 경로 필터 규칙을 $rf.</span><span class="sxs-lookup"><span data-stu-id="39161-110">The second command removes the route filter rule named Rule01 from the route filter stored in $rf.</span></span>

## <span data-ttu-id="39161-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39161-111">PARAMETERS</span></span>

### <span data-ttu-id="39161-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39161-112">-DefaultProfile</span></span>
<span data-ttu-id="39161-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39161-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39161-114">-Force</span><span class="sxs-lookup"><span data-stu-id="39161-114">-Force</span></span>
<span data-ttu-id="39161-115">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39161-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="39161-116">-Name</span><span class="sxs-lookup"><span data-stu-id="39161-116">-Name</span></span>
<span data-ttu-id="39161-117">경로 필터 규칙의 이름</span><span class="sxs-lookup"><span data-stu-id="39161-117">The name of the route filter rule</span></span>

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

### <span data-ttu-id="39161-118">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="39161-118">-RouteFilter</span></span>
<span data-ttu-id="39161-119">The RouteFilter</span><span class="sxs-lookup"><span data-stu-id="39161-119">The RouteFilter</span></span>

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

### <span data-ttu-id="39161-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39161-120">-Confirm</span></span>
<span data-ttu-id="39161-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="39161-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39161-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39161-122">-WhatIf</span></span>
<span data-ttu-id="39161-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="39161-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39161-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39161-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39161-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39161-125">CommonParameters</span></span>
<span data-ttu-id="39161-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="39161-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39161-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="39161-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39161-128">입력</span><span class="sxs-lookup"><span data-stu-id="39161-128">INPUTS</span></span>

### <span data-ttu-id="39161-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="39161-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="39161-130">출력</span><span class="sxs-lookup"><span data-stu-id="39161-130">OUTPUTS</span></span>

### <span data-ttu-id="39161-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="39161-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="39161-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="39161-132">NOTES</span></span>

## <span data-ttu-id="39161-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39161-133">RELATED LINKS</span></span>

[<span data-ttu-id="39161-134">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39161-134">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="39161-135">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39161-135">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="39161-136">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39161-136">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="39161-137">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39161-137">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="39161-138">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="39161-138">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="39161-139">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="39161-139">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="39161-140">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="39161-140">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="39161-141">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="39161-141">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
