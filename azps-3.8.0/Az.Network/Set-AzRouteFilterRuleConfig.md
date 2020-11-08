---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: eb8de50aac1b68928d5cebe8118665b9a24e8fbf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043085"
---
# <span data-ttu-id="4285f-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4285f-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="4285f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4285f-102">SYNOPSIS</span></span>
<span data-ttu-id="4285f-103">경로 필터의 경로 필터 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4285f-103">Modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="4285f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4285f-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4285f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4285f-105">DESCRIPTION</span></span>
<span data-ttu-id="4285f-106">**Set-AzRouteFilterRuleConfig** cmdlet은 경로 필터의 경로 필터 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4285f-106">The **Set-AzRouteFilterRuleConfig** cmdlet modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="4285f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4285f-107">EXAMPLES</span></span>

### <span data-ttu-id="4285f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4285f-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> $rf = Set-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01" -Access Deny -RouteFilterRuleType Community -CommunityList "12076:5010","12076:5040"
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="4285f-109">첫 번째 명령은 RouteFilter01 이라는 경로 필터를 가져와이를 $rf 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4285f-109">The first command gets the route filter named RouteFilter01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="4285f-110">두 번째 명령은 Rule01 이라는 경로 필터 규칙을 수정 하 고 업데이트 된 경로 필터를 $rf 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4285f-110">The second command modifies the route filter rule named Rule01 and stores updated route filter in the $rf variable.</span></span>
<span data-ttu-id="4285f-111">세 번째 명령은 업데이트 된 경로 필터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4285f-111">The third command saves updated route filter.</span></span>

## <span data-ttu-id="4285f-112">변수</span><span class="sxs-lookup"><span data-stu-id="4285f-112">PARAMETERS</span></span>

### <span data-ttu-id="4285f-113">-Access</span><span class="sxs-lookup"><span data-stu-id="4285f-113">-Access</span></span>
<span data-ttu-id="4285f-114">규칙의 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="4285f-114">The access type of the rule.</span></span>
<span data-ttu-id="4285f-115">사용할 수 있는 값은 다음과 같습니다. ' 허용 ', ' 거부 '</span><span class="sxs-lookup"><span data-stu-id="4285f-115">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="4285f-116">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="4285f-116">-CommunityList</span></span>
<span data-ttu-id="4285f-117">경로 필터가 필터링 할 커뮤니티 값 목록</span><span class="sxs-lookup"><span data-stu-id="4285f-117">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="4285f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4285f-118">-DefaultProfile</span></span>
<span data-ttu-id="4285f-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4285f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4285f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4285f-120">-Force</span></span>
<span data-ttu-id="4285f-121">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="4285f-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4285f-122">-이름</span><span class="sxs-lookup"><span data-stu-id="4285f-122">-Name</span></span>
<span data-ttu-id="4285f-123">경로 필터 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4285f-123">The name of the route filter rule</span></span>

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

### <span data-ttu-id="4285f-124">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4285f-124">-RouteFilter</span></span>
<span data-ttu-id="4285f-125">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4285f-125">The RouteFilter</span></span>

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

### <span data-ttu-id="4285f-126">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="4285f-126">-RouteFilterRuleType</span></span>
<span data-ttu-id="4285f-127">규칙의 경로 필터 규칙 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="4285f-127">The route filter rule type of the rule.</span></span>
<span data-ttu-id="4285f-128">사용할 수 있는 값은 다음과 같습니다. ' 커뮤니티 '</span><span class="sxs-lookup"><span data-stu-id="4285f-128">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="4285f-129">-확인</span><span class="sxs-lookup"><span data-stu-id="4285f-129">-Confirm</span></span>
<span data-ttu-id="4285f-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4285f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4285f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4285f-131">-WhatIf</span></span>
<span data-ttu-id="4285f-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4285f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4285f-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4285f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4285f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4285f-134">CommonParameters</span></span>
<span data-ttu-id="4285f-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4285f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4285f-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4285f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4285f-137">입력</span><span class="sxs-lookup"><span data-stu-id="4285f-137">INPUTS</span></span>

### <span data-ttu-id="4285f-138">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4285f-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="4285f-139">출력</span><span class="sxs-lookup"><span data-stu-id="4285f-139">OUTPUTS</span></span>

### <span data-ttu-id="4285f-140">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4285f-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="4285f-141">상속자</span><span class="sxs-lookup"><span data-stu-id="4285f-141">NOTES</span></span>

## <span data-ttu-id="4285f-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4285f-142">RELATED LINKS</span></span>

[<span data-ttu-id="4285f-143">추가-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4285f-143">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4285f-144">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4285f-144">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4285f-145">새로운 AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4285f-145">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4285f-146">제거-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4285f-146">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4285f-147">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4285f-147">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="4285f-148">새로운 AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4285f-148">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="4285f-149">제거-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4285f-149">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="4285f-150">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4285f-150">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
