---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d55c16f7fa4f45ac3b1249f4e2e8b41dfb529d4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204002"
---
# <span data-ttu-id="ebdb2-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ebdb2-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="ebdb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebdb2-102">SYNOPSIS</span></span>
<span data-ttu-id="ebdb2-103">경로 필터의 경로 필터 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ebdb2-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="ebdb2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ebdb2-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebdb2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ebdb2-105">DESCRIPTION</span></span>
<span data-ttu-id="ebdb2-106">**Get-AzRouteFilterRuleConfig** cmdlet은 경로 필터 규칙 또는 경로 필터의 경로 필터 규칙 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ebdb2-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="ebdb2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ebdb2-107">EXAMPLES</span></span>

### <span data-ttu-id="ebdb2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ebdb2-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="ebdb2-109">첫 번째 명령은 MyRouteFilter 이라는 경로 필터를 가져온 다음이를 변수 $rf에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebdb2-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="ebdb2-110">두 번째 명령은 해당 경로 필터와 연결 된 Rule01 이라는 경로 필터 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ebdb2-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="ebdb2-111">세 번째 명령은 해당 경로 필터와 연결 된 경로 필터 규칙의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ebdb2-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="ebdb2-112">변수</span><span class="sxs-lookup"><span data-stu-id="ebdb2-112">PARAMETERS</span></span>

### <span data-ttu-id="ebdb2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebdb2-113">-DefaultProfile</span></span>
<span data-ttu-id="ebdb2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ebdb2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebdb2-115">-이름</span><span class="sxs-lookup"><span data-stu-id="ebdb2-115">-Name</span></span>
<span data-ttu-id="ebdb2-116">경로 필터 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ebdb2-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="ebdb2-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebdb2-117">-RouteFilter</span></span>
<span data-ttu-id="ebdb2-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebdb2-118">The RouteFilter</span></span>

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

### <span data-ttu-id="ebdb2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebdb2-119">CommonParameters</span></span>
<span data-ttu-id="ebdb2-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebdb2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebdb2-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ebdb2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebdb2-122">입력</span><span class="sxs-lookup"><span data-stu-id="ebdb2-122">INPUTS</span></span>

### <span data-ttu-id="ebdb2-123">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ebdb2-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ebdb2-124">출력</span><span class="sxs-lookup"><span data-stu-id="ebdb2-124">OUTPUTS</span></span>

### <span data-ttu-id="ebdb2-125">PSRouteFilterRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ebdb2-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="ebdb2-126">상속자</span><span class="sxs-lookup"><span data-stu-id="ebdb2-126">NOTES</span></span>

## <span data-ttu-id="ebdb2-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ebdb2-127">RELATED LINKS</span></span>

[<span data-ttu-id="ebdb2-128">추가-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ebdb2-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ebdb2-129">새로운 AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ebdb2-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ebdb2-130">제거-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ebdb2-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ebdb2-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ebdb2-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ebdb2-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebdb2-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="ebdb2-133">새로운 AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebdb2-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="ebdb2-134">제거-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebdb2-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="ebdb2-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebdb2-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
