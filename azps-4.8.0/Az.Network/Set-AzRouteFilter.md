---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: f97b9ac971a4eec1945ae4418332e7d6ff74c71c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214314"
---
# <span data-ttu-id="0bb3f-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0bb3f-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="0bb3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bb3f-102">SYNOPSIS</span></span>
<span data-ttu-id="0bb3f-103">경로 필터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb3f-103">Updates a route filter.</span></span>

## <span data-ttu-id="0bb3f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0bb3f-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bb3f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0bb3f-105">DESCRIPTION</span></span>
<span data-ttu-id="0bb3f-106">**Set-AzApplicationGateway** cmdlet은 경로 필터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb3f-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="0bb3f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0bb3f-107">EXAMPLES</span></span>

### <span data-ttu-id="0bb3f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0bb3f-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="0bb3f-109">이 명령은 $rf 변수의 설정을 사용 하 여 경로 필터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb3f-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="0bb3f-110">변수</span><span class="sxs-lookup"><span data-stu-id="0bb3f-110">PARAMETERS</span></span>

### <span data-ttu-id="0bb3f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0bb3f-111">-AsJob</span></span>
<span data-ttu-id="0bb3f-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0bb3f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0bb3f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bb3f-113">-DefaultProfile</span></span>
<span data-ttu-id="0bb3f-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0bb3f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bb3f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0bb3f-115">-Force</span></span>
<span data-ttu-id="0bb3f-116">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="0bb3f-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0bb3f-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="0bb3f-117">-RouteFilter</span></span>
<span data-ttu-id="0bb3f-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="0bb3f-118">The RouteFilter</span></span>

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

### <span data-ttu-id="0bb3f-119">-확인</span><span class="sxs-lookup"><span data-stu-id="0bb3f-119">-Confirm</span></span>
<span data-ttu-id="0bb3f-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb3f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bb3f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bb3f-121">-WhatIf</span></span>
<span data-ttu-id="0bb3f-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0bb3f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0bb3f-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0bb3f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bb3f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bb3f-124">CommonParameters</span></span>
<span data-ttu-id="0bb3f-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb3f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bb3f-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bb3f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bb3f-127">입력</span><span class="sxs-lookup"><span data-stu-id="0bb3f-127">INPUTS</span></span>

### <span data-ttu-id="0bb3f-128">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="0bb3f-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="0bb3f-129">출력</span><span class="sxs-lookup"><span data-stu-id="0bb3f-129">OUTPUTS</span></span>

### <span data-ttu-id="0bb3f-130">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="0bb3f-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="0bb3f-131">상속자</span><span class="sxs-lookup"><span data-stu-id="0bb3f-131">NOTES</span></span>

## <span data-ttu-id="0bb3f-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0bb3f-132">RELATED LINKS</span></span>

[<span data-ttu-id="0bb3f-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0bb3f-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="0bb3f-134">새로운 AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0bb3f-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="0bb3f-135">제거-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0bb3f-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="0bb3f-136">추가-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0bb3f-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0bb3f-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0bb3f-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0bb3f-138">새로운 AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0bb3f-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0bb3f-139">제거-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0bb3f-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0bb3f-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0bb3f-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
