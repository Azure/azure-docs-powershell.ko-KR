---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d66a684b6cd9b26aa9d616a74a4d2eaabaa891ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189641"
---
# <span data-ttu-id="1dad9-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1dad9-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="1dad9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dad9-102">SYNOPSIS</span></span>
<span data-ttu-id="1dad9-103">경로 필터에 대한 경로 필터 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1dad9-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="1dad9-104">구문</span><span class="sxs-lookup"><span data-stu-id="1dad9-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dad9-105">설명</span><span class="sxs-lookup"><span data-stu-id="1dad9-105">DESCRIPTION</span></span>
<span data-ttu-id="1dad9-106">New-AzRouteFilterRuleConfig cmdlet은 Azure 경로 필터에 대한 경로 필터 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1dad9-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="1dad9-107">예제</span><span class="sxs-lookup"><span data-stu-id="1dad9-107">EXAMPLES</span></span>

### <span data-ttu-id="1dad9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1dad9-108">Example 1</span></span>
```powershell
PS C:\> $rule1 = New-AzRouteFilterRuleConfig -Name "Rule01" -Access "Allow" -RouteFilterRuleType "Community" -CommunityList "12076:5040"
```

<span data-ttu-id="1dad9-109">이 명령은 새 경로 필터 규칙을 만들고 변수 $rule 1에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="1dad9-109">The command creates a new route filter rule and stores it in variable $rule1.</span></span>

## <span data-ttu-id="1dad9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dad9-110">PARAMETERS</span></span>

### <span data-ttu-id="1dad9-111">-Access</span><span class="sxs-lookup"><span data-stu-id="1dad9-111">-Access</span></span>
<span data-ttu-id="1dad9-112">경로 필터 규칙에 대한 액세스입니다.</span><span class="sxs-lookup"><span data-stu-id="1dad9-112">Access for route filter rule.</span></span>
<span data-ttu-id="1dad9-113">유효한 값은 허용 또는 거부입니다.</span><span class="sxs-lookup"><span data-stu-id="1dad9-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="1dad9-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="1dad9-114">-CommunityList</span></span>
<span data-ttu-id="1dad9-115">경로 필터가 필터링할 커뮤니티 값 목록</span><span class="sxs-lookup"><span data-stu-id="1dad9-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="1dad9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dad9-116">-DefaultProfile</span></span>
<span data-ttu-id="1dad9-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1dad9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dad9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1dad9-118">-Force</span></span>
<span data-ttu-id="1dad9-119">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dad9-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1dad9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1dad9-120">-Name</span></span>
<span data-ttu-id="1dad9-121">경로 필터 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1dad9-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="1dad9-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="1dad9-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="1dad9-123">경로 필터 규칙 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1dad9-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="1dad9-124">유효한 값은 커뮤니티입니다.</span><span class="sxs-lookup"><span data-stu-id="1dad9-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="1dad9-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1dad9-125">-Confirm</span></span>
<span data-ttu-id="1dad9-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dad9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dad9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dad9-127">-WhatIf</span></span>
<span data-ttu-id="1dad9-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1dad9-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1dad9-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dad9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dad9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dad9-130">CommonParameters</span></span>
<span data-ttu-id="1dad9-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1dad9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dad9-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1dad9-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dad9-133">입력</span><span class="sxs-lookup"><span data-stu-id="1dad9-133">INPUTS</span></span>

### <span data-ttu-id="1dad9-134">없음</span><span class="sxs-lookup"><span data-stu-id="1dad9-134">None</span></span>

## <span data-ttu-id="1dad9-135">출력</span><span class="sxs-lookup"><span data-stu-id="1dad9-135">OUTPUTS</span></span>

### <span data-ttu-id="1dad9-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="1dad9-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="1dad9-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1dad9-137">NOTES</span></span>
<span data-ttu-id="1dad9-138">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="1dad9-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1dad9-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1dad9-139">RELATED LINKS</span></span>

[<span data-ttu-id="1dad9-140">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1dad9-140">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1dad9-141">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1dad9-141">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1dad9-142">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1dad9-142">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1dad9-143">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1dad9-143">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1dad9-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1dad9-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="1dad9-145">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1dad9-145">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="1dad9-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1dad9-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="1dad9-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1dad9-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
