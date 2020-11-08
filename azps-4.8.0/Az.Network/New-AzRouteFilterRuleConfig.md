---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d66a684b6cd9b26aa9d616a74a4d2eaabaa891ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211556"
---
# <span data-ttu-id="cde8a-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cde8a-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="cde8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cde8a-102">SYNOPSIS</span></span>
<span data-ttu-id="cde8a-103">경로 필터에 대 한 경로 필터 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cde8a-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="cde8a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cde8a-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cde8a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cde8a-105">DESCRIPTION</span></span>
<span data-ttu-id="cde8a-106">New-AzRouteFilterRuleConfig cmdlet은 Azure 경로 필터에 대 한 경로 필터 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cde8a-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="cde8a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cde8a-107">EXAMPLES</span></span>

### <span data-ttu-id="cde8a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cde8a-108">Example 1</span></span>
```powershell
PS C:\> $rule1 = New-AzRouteFilterRuleConfig -Name "Rule01" -Access "Allow" -RouteFilterRuleType "Community" -CommunityList "12076:5040"
```

<span data-ttu-id="cde8a-109">명령이 새 경로 필터 규칙을 만들어 변수 $rule 1에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cde8a-109">The command creates a new route filter rule and stores it in variable $rule1.</span></span>

## <span data-ttu-id="cde8a-110">변수</span><span class="sxs-lookup"><span data-stu-id="cde8a-110">PARAMETERS</span></span>

### <span data-ttu-id="cde8a-111">-Access</span><span class="sxs-lookup"><span data-stu-id="cde8a-111">-Access</span></span>
<span data-ttu-id="cde8a-112">경로 필터 규칙에 대 한 액세스입니다.</span><span class="sxs-lookup"><span data-stu-id="cde8a-112">Access for route filter rule.</span></span>
<span data-ttu-id="cde8a-113">유효한 값은 허용 또는 거부입니다.</span><span class="sxs-lookup"><span data-stu-id="cde8a-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="cde8a-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="cde8a-114">-CommunityList</span></span>
<span data-ttu-id="cde8a-115">경로 필터가 필터링 할 커뮤니티 값 목록</span><span class="sxs-lookup"><span data-stu-id="cde8a-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="cde8a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cde8a-116">-DefaultProfile</span></span>
<span data-ttu-id="cde8a-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cde8a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cde8a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="cde8a-118">-Force</span></span>
<span data-ttu-id="cde8a-119">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="cde8a-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="cde8a-120">-이름</span><span class="sxs-lookup"><span data-stu-id="cde8a-120">-Name</span></span>
<span data-ttu-id="cde8a-121">경로 필터 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cde8a-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="cde8a-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="cde8a-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="cde8a-123">경로 필터 규칙 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="cde8a-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="cde8a-124">유효한 값은 다음과 같습니다. 커뮤니티</span><span class="sxs-lookup"><span data-stu-id="cde8a-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="cde8a-125">-확인</span><span class="sxs-lookup"><span data-stu-id="cde8a-125">-Confirm</span></span>
<span data-ttu-id="cde8a-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cde8a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cde8a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cde8a-127">-WhatIf</span></span>
<span data-ttu-id="cde8a-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cde8a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cde8a-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cde8a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cde8a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cde8a-130">CommonParameters</span></span>
<span data-ttu-id="cde8a-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cde8a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cde8a-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cde8a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cde8a-133">입력</span><span class="sxs-lookup"><span data-stu-id="cde8a-133">INPUTS</span></span>

### <span data-ttu-id="cde8a-134">않아야</span><span class="sxs-lookup"><span data-stu-id="cde8a-134">None</span></span>

## <span data-ttu-id="cde8a-135">출력</span><span class="sxs-lookup"><span data-stu-id="cde8a-135">OUTPUTS</span></span>

### <span data-ttu-id="cde8a-136">PSRouteFilterRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="cde8a-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="cde8a-137">상속자</span><span class="sxs-lookup"><span data-stu-id="cde8a-137">NOTES</span></span>
<span data-ttu-id="cde8a-138">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="cde8a-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="cde8a-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cde8a-139">RELATED LINKS</span></span>

[<span data-ttu-id="cde8a-140">추가-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cde8a-140">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="cde8a-141">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cde8a-141">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="cde8a-142">제거-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cde8a-142">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="cde8a-143">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cde8a-143">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="cde8a-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cde8a-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="cde8a-145">새로운 AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cde8a-145">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="cde8a-146">제거-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cde8a-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="cde8a-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cde8a-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
