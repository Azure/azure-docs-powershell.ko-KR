---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d55c16f7fa4f45ac3b1249f4e2e8b41dfb529d4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369923"
---
# <span data-ttu-id="ec84c-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ec84c-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="ec84c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec84c-102">SYNOPSIS</span></span>
<span data-ttu-id="ec84c-103">경로 필터에서 경로 필터 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec84c-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="ec84c-104">구문</span><span class="sxs-lookup"><span data-stu-id="ec84c-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec84c-105">설명</span><span class="sxs-lookup"><span data-stu-id="ec84c-105">DESCRIPTION</span></span>
<span data-ttu-id="ec84c-106">**Get-AzRouteFilterRuleConfig** cmdlet은 경로 필터 규칙 또는 경로 필터 규칙 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec84c-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="ec84c-107">예제</span><span class="sxs-lookup"><span data-stu-id="ec84c-107">EXAMPLES</span></span>

### <span data-ttu-id="ec84c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ec84c-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="ec84c-109">첫 번째 명령은 MyRouteFilter라는 경로 필터를 찍은 다음, 변수에 $rf.</span><span class="sxs-lookup"><span data-stu-id="ec84c-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="ec84c-110">두 번째 명령은 해당 경로 필터와 연결된 Rule01이라는 경로 필터 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec84c-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="ec84c-111">세 번째 명령은 해당 경로 필터와 연결된 경로 필터 규칙 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec84c-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="ec84c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec84c-112">PARAMETERS</span></span>

### <span data-ttu-id="ec84c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec84c-113">-DefaultProfile</span></span>
<span data-ttu-id="ec84c-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec84c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec84c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ec84c-115">-Name</span></span>
<span data-ttu-id="ec84c-116">경로 필터 규칙의 이름</span><span class="sxs-lookup"><span data-stu-id="ec84c-116">The name of the route filter rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec84c-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ec84c-117">-RouteFilter</span></span>
<span data-ttu-id="ec84c-118">The RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ec84c-118">The RouteFilter</span></span>

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

### <span data-ttu-id="ec84c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec84c-119">CommonParameters</span></span>
<span data-ttu-id="ec84c-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec84c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec84c-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ec84c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec84c-122">입력</span><span class="sxs-lookup"><span data-stu-id="ec84c-122">INPUTS</span></span>

### <span data-ttu-id="ec84c-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ec84c-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ec84c-124">출력</span><span class="sxs-lookup"><span data-stu-id="ec84c-124">OUTPUTS</span></span>

### <span data-ttu-id="ec84c-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="ec84c-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="ec84c-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ec84c-126">NOTES</span></span>

## <span data-ttu-id="ec84c-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec84c-127">RELATED LINKS</span></span>

[<span data-ttu-id="ec84c-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ec84c-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ec84c-129">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ec84c-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ec84c-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ec84c-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ec84c-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ec84c-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ec84c-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ec84c-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="ec84c-133">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ec84c-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="ec84c-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ec84c-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="ec84c-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ec84c-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
