---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: e596ea3092cd5fda045c20f80c9208015b57a42d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043989"
---
# <span data-ttu-id="7fb75-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7fb75-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="7fb75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fb75-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb75-103">경로 필터에서 경로 필터 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb75-103">Removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="7fb75-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7fb75-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fb75-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7fb75-105">DESCRIPTION</span></span>
<span data-ttu-id="7fb75-106">**AzRouteFilterRuleConfig** cmdlet은 경로 필터에서 경로 필터 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb75-106">The **Remove-AzRouteFilterRuleConfig** cmdlet removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="7fb75-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7fb75-107">EXAMPLES</span></span>

### <span data-ttu-id="7fb75-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7fb75-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
```

<span data-ttu-id="7fb75-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 RouteFilter01 이라는 경로 필터를 가져온 다음이를 $rf 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb75-109">The first command gets a route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="7fb75-110">두 번째 명령은 $rf에 저장 된 경로 필터에서 Rule01 이라는 경로 필터 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb75-110">The second command removes the route filter rule named Rule01 from the route filter stored in $rf.</span></span>

## <span data-ttu-id="7fb75-111">변수</span><span class="sxs-lookup"><span data-stu-id="7fb75-111">PARAMETERS</span></span>

### <span data-ttu-id="7fb75-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb75-112">-DefaultProfile</span></span>
<span data-ttu-id="7fb75-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7fb75-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fb75-114">-Force</span><span class="sxs-lookup"><span data-stu-id="7fb75-114">-Force</span></span>
<span data-ttu-id="7fb75-115">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="7fb75-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7fb75-116">-이름</span><span class="sxs-lookup"><span data-stu-id="7fb75-116">-Name</span></span>
<span data-ttu-id="7fb75-117">경로 필터 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fb75-117">The name of the route filter rule</span></span>

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

### <span data-ttu-id="7fb75-118">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="7fb75-118">-RouteFilter</span></span>
<span data-ttu-id="7fb75-119">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="7fb75-119">The RouteFilter</span></span>

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

### <span data-ttu-id="7fb75-120">-확인</span><span class="sxs-lookup"><span data-stu-id="7fb75-120">-Confirm</span></span>
<span data-ttu-id="7fb75-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb75-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fb75-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fb75-122">-WhatIf</span></span>
<span data-ttu-id="7fb75-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7fb75-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7fb75-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7fb75-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fb75-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb75-125">CommonParameters</span></span>
<span data-ttu-id="7fb75-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb75-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb75-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fb75-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb75-128">입력</span><span class="sxs-lookup"><span data-stu-id="7fb75-128">INPUTS</span></span>

### <span data-ttu-id="7fb75-129">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7fb75-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="7fb75-130">출력</span><span class="sxs-lookup"><span data-stu-id="7fb75-130">OUTPUTS</span></span>

### <span data-ttu-id="7fb75-131">PSRouteFilterRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7fb75-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="7fb75-132">상속자</span><span class="sxs-lookup"><span data-stu-id="7fb75-132">NOTES</span></span>

## <span data-ttu-id="7fb75-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7fb75-133">RELATED LINKS</span></span>

[<span data-ttu-id="7fb75-134">추가-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7fb75-134">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7fb75-135">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7fb75-135">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7fb75-136">새로운 AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7fb75-136">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7fb75-137">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7fb75-137">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7fb75-138">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7fb75-138">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="7fb75-139">새로운 AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7fb75-139">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="7fb75-140">제거-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7fb75-140">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="7fb75-141">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7fb75-141">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
